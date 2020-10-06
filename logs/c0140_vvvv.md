---
title: "c0140_vvvv"
date: 2020-10-07T00:11:25+1010:00
draft: false
weight: 11403

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0140
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
    loading [Task]:  ./tests/functests/c0140
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
    Task1: [task ==> task: main entry ]
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
    I am the main entry
    
```

##### Logs with different verbose level
* [c0140 log - verbose level v](../../logs/c0140_v)
* [c0140 log - verbose level vv](../../logs/c0140_vv)
* [c0140 log - verbose level vvv](../../logs/c0140_vvv)
* [c0140 log - verbose level vvvv](../../logs/c0140_vvvv)
* [c0140 log - verbose level vvvvv](../../logs/c0140_vvvvv)

##### References
* [Related Chapter](../../usage/c0140)
