## Redux for angular

### Store

 - is configured at bootstrap
 - can be then injected into components/services
 - may have multiple sub-stores
  - *boostrap(App, [provideStore({reducer1, reducer2})])*

### Selector
The Selector function takes as input the application state and returns from it a specific View Model.

### Effects

### Reducer

Best practices:
  - use constants instead of plain strings
  - expand the reducers to use rich objects as parameters, to enable a richer payload

### Local browser storage backing
RxJS powered IndexedDB for Angular apps
@ngrx/db - currently not production ready.



Credits, sources and some links of interest for further reading:
--
* http://blog.angular-university.io/angular-ngrx-store-and-effects-crash-course/
