---
title: "c0138_vvvv"
date: 2020-10-07T00:11:24+1010:00
draft: false
weight: 11383

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0138
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
    loading [Task]:  ./tests/functests/c0138
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
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    ~SubStep2: [print:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep3: [print:  ]
    step3
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    ~SubStep2: [:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep3: [:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep4: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    step5
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [temporarily deactivated]
    
```

##### Logs with different verbose level
* [c0138 log - verbose level v](../../logs/c0138_v)
* [c0138 log - verbose level vv](../../logs/c0138_vv)
* [c0138 log - verbose level vvv](../../logs/c0138_vvv)
* [c0138 log - verbose level vvvv](../../logs/c0138_vvvv)
* [c0138 log - verbose level vvvvv](../../logs/c0138_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0138)
