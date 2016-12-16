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
---
Credits, sources and some links of interest for further reading:
==
