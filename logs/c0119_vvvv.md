---
title: "c0119_vvvv"
date: 2020-09-18T01:27:41+99:00
draft: false
weight: 11193

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0119
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0119
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [step1: demo it will loop until loopitem = item3 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    item1
    ~SubStep1: [print:  ]
    item2
    loop util conditional break
    
    -Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    hello
    -Step3: [step3:  ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 1
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 2
    loop util conditional break
    
    -Step4: [step4:  ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1"
    })
    
    ~~SubStep1: [print:  ]
    proc 1
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 2
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~~SubStep1: [print:  ]
    proc 3
    loop util conditional break
    
    -Step5: [step5: it will stop loop at proc 4 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    ~~SubStep1: [print:  ]
    person: jason
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    person: jason
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~~SubStep1: [print:  ]
    person: jason
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3
    })
    
    ~~SubStep1: [reg:  ]
    --Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "tom",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    ~~SubStep1: [print:  ]
    person: tom
    loop util conditional break
    
    
```

##### Logs with different verbose level
* [c0119 log - verbose level v](../../logs/c0119_v)
* [c0119 log - verbose level vv](../../logs/c0119_vv)
* [c0119 log - verbose level vvv](../../logs/c0119_vvv)
* [c0119 log - verbose level vvvv](../../logs/c0119_vvvv)
* [c0119 log - verbose level vvvvv](../../logs/c0119_vvvvv)

##### References
* [Related Chapter](../../loop/c0119)
