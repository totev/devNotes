### Deploy only a function
	sls --region eu-central-1 deploy function --function $FUNCTION_NAME
	
### Run a function
	sls --region eu-central-1 invoke --function helloWorld --log
	
	
### Cloudflare <-> AWS Api gateway
https://stackoverflow.com/questions/36737313/how-to-cname-to-amazon-api-gateway-endpoint/45849093#45849093

There are several reasons why it doens't work to simply point Cloudflare at your API Gateway domain and call it a day:

    API Gateway uses shared hosting so it uses the domain name to figure out what API to send requests to. It has no way of knowing that api.yourdomain.com belongs to your API.
    API Gateway requires that you use https, but the certificate that it uses is only valid for the default domain.

There is a solution, however. Here are the steps that I followed when I recently set this up:

* Generate an origin certificate from the crypto tab of the Cloudflare dashboard.
* Import the certificate to AWS Certificate manager in the us-east-1 region, even if your API is located in a different region. If you are prompted for the certificate chain you can copy it from here<https://support.cloudflare.com/hc/en-us/articles/218689638-What-are-the-root-certificate-authorities-CAs-used-with-CloudFlare-Origin-CA->.
* Add your custom domain in the API Gateway console and select the certificate you just added. Check the AWS support article for more information on how to do this.
* It usually takes about 45 minutes for the custom domain to finish initializing. Once it's done it will give you a new Cloudfront URL. Go ahead and make sure your API still works through this new URL.
* Go to the Cloudflare DNS tab and setup a CNAME record pointing to Cloudfront URL you just created.
* Switch to the crypto tab and set your SSL mode to "Full (Strict)". If you skip this step you'll get a redirect loop.

That's it. Enjoy your new highly available API served from your custom domain!
