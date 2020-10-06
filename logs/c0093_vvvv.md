---
title: "c0093_vvvv"
date: 2020-10-07T00:11:15+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0093
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "person": {
        "name": "tom",
        "age": 23
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "person": {
        "age": 23,
        "name": "tom"
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
      "up_runtime_task_layer_number": 1,
      "person": {
        "name": "tom",
        "age": 23
      }
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
