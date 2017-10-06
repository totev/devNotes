## Do it reactively

# Operators
  - do *merge* the streams
  - *startWith* and *scan* can be used to create a state vector
  - *withLatestFrom* combines two observables and may extract their last emitted value
  - *distinctUntilChanged* supresses duplicate items
  - *share* creates an intermediate subject allowing multiple subscriptions to the same observable without recreating it's source upon new subscriptions => multicasting
  - *interval* emits every XX millis
  - *skip* skips SURPRISE x emitted values
  - *do* executes a lambda
  


Credits, sources and some links of interest for further reading:
--
* https://egghead.io/courses/build-redux-style-applications-with-angular-rxjs-and-ngrx-store  
* https://blog.thoughtram.io/rxjs/2017/08/24/taming-snakes-with-reactive-streams.html
