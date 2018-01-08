# Vue.js (pronounced like view) is a progressive framework for building user interfaces.

## Intro


## Stated facts
 - virtual dom based
 - Vue embraces classic web technologies and builds on top of them
 - need for speed (size/performance/change-detection/data binding)



## Documentation
Clear and nice documentation on the main site. Nothing overcomplicated.

## Code splitting
Best use case - Routes

Some usecases:

 - Route
 	- via async import: `const Something = () => import('@/page/Something') 
 - Component
 	- via async import
 - Lifecycle
 	- via async import, conditional
	
	
## Progressive Web Applications
	vue init pwa new-project	

Caveats:

 - ServiceWorkers can't use websockets 
 
## E2E Testing



## Tools
 
Testing:

 - vue-test-utils -> will soon become the official test package
 - eslint-plugin-vue -> template support  
 - vue-cli 3.0
 

Credits, sources and some links of interest for further reading:
--
* https://vuejs.org/v2/guide/
* https://alexjoverm.github.io/2017/06/28/Integrate-TypeScript-in-your-Vue-project/