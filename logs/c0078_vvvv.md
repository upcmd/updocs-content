---
title: "c0078_vvvv"
date: 2020-10-06T23:46:04+1010:00
draft: false
weight: 10783

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0078
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
    loading [Task]:  ./tests/functests/c0078
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
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_name": "sydney grammar"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000",
      "up_runtime_task_layer_number": 0,
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_name": "sydney grammar"
    })
    
    ~SubStep1: [print:  ]
    sydney grammar
    ~SubStep2: [print:  ]
    sydney grammar : 1 fox road, sydney, nsw 2000
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    None
    
```

##### Logs with different verbose level
* [c0078 log - verbose level v](../../logs/c0078_v)
* [c0078 log - verbose level vv](../../logs/c0078_vv)
* [c0078 log - verbose level vvv](../../logs/c0078_vvv)
* [c0078 log - verbose level vvvv](../../logs/c0078_vvvv)
* [c0078 log - verbose level vvvvv](../../logs/c0078_vvvvv)

##### References
* [Related Chapter](../../dvars/c0078)
