Two way binding:
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
