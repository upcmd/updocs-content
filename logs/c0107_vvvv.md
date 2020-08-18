---
title: "c0107_vvvv"
date: 2020-08-18T15:16:09+88:00
draft: false
weight: 11073

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0107
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
    loading [Task]:  ./tests/functests/c0107
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
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    })
    
      located task-> 2 [sub]: 
    =Task2: [task ==> sub:  ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "john": "john in sub func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [reg:  ]
    ~~SubStep2: [print:  ]
    in sub print1: tom created in sub
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in global",
      "tom": "tom created in sub"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in sub",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [trace:  ]
    Trace:debug tom's value==>
    --Step3: [: check value of tom 2 ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub func2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "john": "john in sub func2",
      "tom": "tom created in sub",
      "jerry": "this is jerry in global"
    })
    
    ~~SubStep1: [print:  ]
    in sub print2: tom created in sub
    --Step4:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [trace:  ]
    Trace:<==debug tom's value
    -Step2: [: check value of tom ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [print:  ]
    in main task print3: this is tom in global
    
```

##### Logs with different verbose level
* [c0107 log - verbose level v](../../logs/c0107_v)
* [c0107 log - verbose level vv](../../logs/c0107_vv)
* [c0107 log - verbose level vvv](../../logs/c0107_vvv)
* [c0107 log - verbose level vvvv](../../logs/c0107_vvvv)
* [c0107 log - verbose level vvvvv](../../logs/c0107_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0107)
