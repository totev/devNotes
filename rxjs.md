rxjs a.k.a the brainfuck reactive framework
=======
Some words of advice, before using this framework:



Higher order observables
=======
Clarification: higher order observables => observables which emit observables

* Flattening operators:
  *  switch
            -> Observable[Observable<any>] => Observable<any>
            -> switches to the latest Observable upon its firing
            AND unsubscribes from the previous one
 * mergeAll(numOfObs:number)
          -> merges all of the inner observables concurrently (duh)
          -> the param "numOfObs" limits the max number of observables to which one can subscribe concurrently. If some of the subscribed ones complete, then this thing will subscribe to newly created ones - otherwise nothing will happen upon spawning new observables
 * contcatAll == mergeAll(1)
        -> subscribe to at most 1 observable, gather the ones created afterwards and upon the completion of the subscribed one, subscribe automatically to the next one
 *



Credits, sources and some links of interest for further reading:
==
* https://egghead.io/courses/use-higher-order-observables-in-rxjs-effectively
