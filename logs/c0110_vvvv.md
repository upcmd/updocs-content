---
title: "c0110_vvvv"
date: 2020-08-09T01:36:15+88:00
draft: false
weight: 11103

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0110
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0110
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0
    })
    
    ~~SubStep1: [print:  ]
    1:tom
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .loopitem "tom"}}]
    --Step3:
    current exec runtime vars:
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom"
    })
    
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "loopitem": "tom",
      "up_runtime_task_layer_number": 1,
      "theone": "tom"
    })
    
    ~~SubStep1: [print:  ]
    tom
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    2:jerry
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    --Step3:
    current exec runtime vars:
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "jerry"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "theone": "jerry"
    })
    
    ~~SubStep1: [print:  ]
    jerry
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    3:emily
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    --Step3:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopindex1": 3,
      "loopitem": "emily"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopindex1": 3,
      "loopitem": "emily",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "theone": "emily"
    })
    
    ~~SubStep1: [print:  ]
    emily
    
```

##### Logs with different verbose level
* [c0110 log - verbose level v](../../logs/c0110_v)
* [c0110 log - verbose level vv](../../logs/c0110_vv)
* [c0110 log - verbose level vvv](../../logs/c0110_vvv)
* [c0110 log - verbose level vvvv](../../logs/c0110_vvvv)
* [c0110 log - verbose level vvvvv](../../logs/c0110_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0110)
