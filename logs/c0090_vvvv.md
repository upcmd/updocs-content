---
title: "c0090_vvvv"
date: 2020-10-07T00:11:15+1010:00
draft: false
weight: 10903

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0090
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
    loading [Task]:  ./tests/functests/c0090
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    wrong_usagenote that you can't access loopitem in dvar processing in curent func
    you can only access loopitem in dvar processing when it is called as callee, as corret_usage shows
    however you can access loopitem in do action
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    dvar> person:
    "None"
    
    -
    None
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "person": "None"
    })
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: tom
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: peter
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: james
    
    -Step2: [corret_usage:  ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "taskvar": "taskvar"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "taskvar": "taskvar"
    })
    
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar"
    })
    
    dvar> person:
    "tom"
    
    -
    tom
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "tom",
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: tom
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: tom
    ~~SubStep3: [print:  ]
    callee2: <no value>
    ~~SubStep4: [print:  ]
    taskvar: taskvar
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    dvar> person:
    "peter"
    
    -
    peter
    self: final context exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "peter"
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: peter
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: peter
    ~~SubStep3: [print:  ]
    callee2: <no value>
    ~~SubStep4: [print:  ]
    taskvar: taskvar
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "james",
      "loopindex": 2
    })
    
    dvar> person:
    "james"
    
    -
    james
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "james",
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: james
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: james
    ~~SubStep3: [print:  ]
    callee2: <no value>
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    
```

##### Logs with different verbose level
* [c0090 log - verbose level v](../../logs/c0090_v)
* [c0090 log - verbose level vv](../../logs/c0090_vv)
* [c0090 log - verbose level vvv](../../logs/c0090_vvv)
* [c0090 log - verbose level vvvv](../../logs/c0090_vvvv)
* [c0090 log - verbose level vvvvv](../../logs/c0090_vvvvv)

##### References
* [Related Chapter](../../loop/c0090)
