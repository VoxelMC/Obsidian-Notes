# Tasks
All available tasks from lecture notes are listed below.

## CHEM211
```dataviewjs
const Tasks = dv.pages("#CHEM211").file.tasks;

let CompletedTasks = Tasks.where(t => t.completed) || 0;
let tryPercentage = (CompletedTasks.length / Tasks.length) * 100;
let percentage = !Number.isNaN(tryPercentage) ? tryPercentage : 0; 

dv.span("![progress](https://progress-bar.dev/" + percentage + "/?title=CHEM211&width=80" + ")" 
);

```
```dataview
task from #CHEM211
```

## BIOL366
```dataviewjs
const Tasks = dv.pages("#BIOL366").file.tasks;

let CompletedTasks = Tasks.where(t => t.completed) || 0;
let tryPercentage = (CompletedTasks.length / Tasks.length) * 100;
let percentage = !Number.isNaN(tryPercentage) ? tryPercentage : 0; 

dv.span("![progress](https://progress-bar.dev/" + percentage + "/?title=BIOL366&width=80" + ")" 
);

```
```dataview
task from #BIOL366 
```

## BIOC412
```dataviewjs
const Tasks = dv.pages("#BIOC412").file.tasks;

let CompletedTasks = Tasks.where(t => t.completed) || 0;
let tryPercentage = (CompletedTasks.length / Tasks.length) * 100;
let percentage = !Number.isNaN(tryPercentage) ? tryPercentage : 0; 

dv.span("![progress](https://progress-bar.dev/" + percentage + "/?title=BIOC412&width=80" + ")" 
);

```
```dataview
task from #BIOC412
```

## BIOC425
```dataviewjs
const Tasks = dv.pages("#BIOC425").file.tasks;

let CompletedTasks = Tasks.where(t => t.completed) || 0;
let tryPercentage = (CompletedTasks.length / Tasks.length) * 100;
let percentage = !Number.isNaN(tryPercentage) ? tryPercentage : 0; 

dv.span("![progress](https://progress-bar.dev/" + percentage + "/?title=BIOC425&width=80" + ")" 
);

```
```dataview
task from #BIOC425
```

## ENGL395B
```dataviewjs
const Tasks = dv.pages("#ENGL395B").file.tasks;

let CompletedTasks = Tasks.where(t => t.completed) || 0;
let tryPercentage = (CompletedTasks.length / Tasks.length) * 100;
let percentage = !Number.isNaN(tryPercentage) ? tryPercentage : 0; 

dv.span("![progress](https://progress-bar.dev/" + percentage + "/?title=ENGL395B&width=80" + ")" 
);

```
```dataview
task from #ENGL395B
```


