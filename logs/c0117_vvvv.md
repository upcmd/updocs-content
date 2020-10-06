---
title: "c0117_vvvv"
date: 2020-10-07T00:11:20+1010:00
draft: false
weight: 11173

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0117
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0117
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [step2: call subtask and exam the return value in following steps ]
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
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 1
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "parentLoopItem": "proc 1",
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item2
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item3
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    proc 2
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "parentLoopItem": "proc 2"
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item2
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item3
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 3
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "parentLoopItem": "proc 3"
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item2
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item3
    
```

##### Logs with different verbose level
* [c0117 log - verbose level v](../../logs/c0117_v)
* [c0117 log - verbose level vv](../../logs/c0117_vv)
* [c0117 log - verbose level vvv](../../logs/c0117_vvv)
* [c0117 log - verbose level vvvv](../../logs/c0117_vvvv)
* [c0117 log - verbose level vvvvv](../../logs/c0117_vvvvv)

##### References
* [Related Chapter](../../loop/c0117)
