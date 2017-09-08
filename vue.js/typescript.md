# Vue.js with typescript = Vue.ts


## Tools
 - vue-property-decorator
 	- @Prop for property binding
	- @Model
	- @Watch
	- @Inject, @Provide
	- createDecorator
 - inversify
 - reflect-metadata

## Class hierarchy

 - hooks are called on all classes (parent + child) this is the default vue.js merging strategy
 - methods are being overriten (default ts behaviuor)
 - additional hooks (like the router ones) need to be registered before loading the app (e.g. in hooks.ts)
 
 
## Two way binding
Use the @Model decorator.


## Value change observation
@Watch for primitive type watching, {deep:true} for object (props) watching

## Dependency injection
How to use:

 - annotate a service with @Provide on the highest hierarchy possible 
 - annotate a field with @Inject in the class/component where the service is to be use/consumed

Best practices:

 - use global deps on app level and not on component level
 
## IoC
Using *inversify* and *reflect-metadata*.

Create a *container.ts*

## Custom decorators
Just use the *createDecorator* factory provided.

## AOP
May be done with *kaop-ts*.