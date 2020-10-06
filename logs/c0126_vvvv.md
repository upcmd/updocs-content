---
title: "c0126_vvvv"
date: 2020-10-07T00:11:22+1010:00
draft: false
weight: 11263

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0126
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
    loading [Task]:  ./tests/functests/c0126
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
      "goahead": false
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "goahead": false
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
    true
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [else]: 
    =Task3: [task ==> else:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    do something else .......
    
```

##### Logs with different verbose level
* [c0126 log - verbose level v](../../logs/c0126_v)
* [c0126 log - verbose level vv](../../logs/c0126_vv)
* [c0126 log - verbose level vvv](../../logs/c0126_vvv)
* [c0126 log - verbose level vvvv](../../logs/c0126_vvvv)
* [c0126 log - verbose level vvvvv](../../logs/c0126_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0126)
