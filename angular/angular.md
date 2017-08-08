angular 2.x, 3.x, 4.x and god knows which new version
====

Two way binding in components:
    <bam [(roar)]></bam>

    @Component({
      selector: 'bam',
      template: `
        <span>{{roar}}</span>
      `
    })
    export class BamComponent{

    @Input()
    roar:string;

    @Output()
    roarChange = new EventEmitter();

      private doStuff(){
        this.roar = "wow!";
        //magic
        this.roarChange.emit(this.roar);
      }

    }
    // another alternative without any component configuration
    <input [value]="data" (input)="data = $event.target.value" />


## Component

Nice/nifty things to know:
  - the async pipe automagically subscribes to a given observable and *unsubscribes* afterwards/upon component destruction
  - all pipes can be concatenated, but the async one is the most fun!

### Component projection
http://blog.angular-university.io/angular-ng-content/


### Component Design
http://blog.angular-university.io/angular-component-design-how-to-avoid-custom-event-bubbling-and-extraneous-properties-in-the-local-component-tree/

http://blog.angular-university.io/onpush-change-detection-how-it-works/

CSS
===
Try to use component based styles mixed with the global ones for better encapsulation and separation of concerns.

---
Credits, sources and some links of interest for further reading:
==
* https://egghead.io/courses/build-redux-style-applications-with-angular-rxjs-and-ngrx-store
