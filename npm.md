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