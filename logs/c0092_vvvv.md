---
title: "c0092_vvvv"
date: 2020-08-18T15:16:05+88:00
draft: false
weight: 10923

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0092
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
    loading [Task]:  ./tests/functests/c0092
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
      "person": {
        "name": "tom",
        "age": 23
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
        "name": "tom",
        "age": 23
      },
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello tom
    
```

##### Logs with different verbose level
* [c0092 log - verbose level v](../../logs/c0092_v)
* [c0092 log - verbose level vv](../../logs/c0092_vv)
* [c0092 log - verbose level vvv](../../logs/c0092_vvv)
* [c0092 log - verbose level vvvv](../../logs/c0092_vvvv)
* [c0092 log - verbose level vvvvv](../../logs/c0092_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0092)
