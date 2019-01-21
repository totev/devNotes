NPM
===
Check if a given package is installed.

	npm ls package-name
	
This is much cleaneer than doing ```ls node_modules/package-name``` or ```cat node_modules/package-name/package.json | grep version```.

Also npm ls can check if a given module is installed globally by adding ```--global``` to the command.

NPX
---
Temporary install a package.
@version uses a dedicated version of the package.
-p add packages to the temporary environment. This is particulary helpful to try running code in different versions of node.

NPM VIEW
---
Show latest module version.


Node
===
Useful packages:

 * nodemon
  * watching for changes ```nodemon index.js```
 * commander
```
	 const program = require('commander');
	 program
	 .version(pkg.version)
	 .description(pkg.description)
	 .usage('[options] <command> [...]')
	 .option('-o, --host <hostname>', 'hostname [localhost]', 'localhost') .option('-p, --port <number>', 'port number [9200]', '9200') .option('-j, --json', 'format output as JSON')
	 .option('-i, --index <name>', 'which index to use')
	 .option('-t, --type <type>', 'default type for bulk operations');
```