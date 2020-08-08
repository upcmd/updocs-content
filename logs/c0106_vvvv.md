---
title: "c0106_vvvv"
date: 2020-08-09T01:36:14+88:00
draft: false
weight: 11063

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0106
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
    loading [Task]:  ./tests/functests/c0106
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
      "tom": "this is tom"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
      located task-> 2 [sub1]: 
    =Task2: [task ==> sub1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [reg:  ]
    ~~SubStep2: [print:  ]
    hello, this is tom
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print: should be <no value> since it is marked localOnly ]
    None
    -Step2: [: check if hitom is available in global context
    it should be <no value> as hitom in sub1 is marked localOnly
     ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [print:  ]
    None
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [sub2]: 
    =Task3: [task ==> sub2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [reg:  ]
    ~~SubStep2: [print:  ]
    hello, this is tom
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom",
      "tom": "this is tom"
    })
    
    ~~SubStep1: [print: by default hitom is accessible from global context, that's why it is accessiable cross func
    however this is only available in its own call stack global but not return and available to its parent var scope
     ]
    hello, this is tom
    -Step4: [: check if hitom is available in global context
    though hitom was regiser as global var, but it was registered to its own call stack
    however this is only available in its own call stack global but not return and available to its parent var scope
     ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [print:  ]
    None
    
```

##### Logs with different verbose level
* [c0106 log - verbose level v](../../logs/c0106_v)
* [c0106 log - verbose level vv](../../logs/c0106_vv)
* [c0106 log - verbose level vvv](../../logs/c0106_vvv)
* [c0106 log - verbose level vvvv](../../logs/c0106_vvvv)
* [c0106 log - verbose level vvvvv](../../logs/c0106_vvvvv)

##### References
* [Related Chapter](../../vars/c0106)
