---
title: "c0078_vvvv"
date: 2020-07-20T02:01:43+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0078
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
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000",
      "school_name": "sydney grammar"
    })
    
    ~SubStep1: [print:  ]
    sydney grammar
    ~SubStep2: [print:  ]
    sydney grammar : 1 fox road, sydney, nsw 2000
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
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
