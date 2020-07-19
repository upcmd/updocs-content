---
title: "c0093_vvvv"
date: 2020-07-20T02:01:45+77:00
draft: false
weight: 10933

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0093
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0093
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
      "person": {
        "age": 23,
        "name": "tom"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 23
      }
    })
    
      located task-> 2 [tom_action]: 
    =Task2: [task ==> tom_action:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 23
      },
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "age": 23,
        "name": "tom"
      },
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello tom
    
```

##### Logs with different verbose level
* [c0093 log - verbose level v](../../logs/c0093_v)
* [c0093 log - verbose level vv](../../logs/c0093_vv)
* [c0093 log - verbose level vvv](../../logs/c0093_vvv)
* [c0093 log - verbose level vvvv](../../logs/c0093_vvvv)
* [c0093 log - verbose level vvvvv](../../logs/c0093_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0093)
