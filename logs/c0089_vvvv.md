---
title: "c0089_vvvv"
date: 2020-10-06T23:46:06+1010:00
draft: false
weight: 10893

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0089
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
    loading [Task]:  ./tests/functests/c0089
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
      "dynadir": "./tests/functests"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "dynadir": "./tests/functests"
    })
    
    loading [flow ref]:  ./tests/functests/c0089-task-main.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "dynadir": "./tests/functests",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "dynadir": "./tests/functests",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "task step 1"
    
    cmd=>:
    echo "task step 1"
    -
    task step 1
    
    -
     .. ok
    cmd( 2):
    echo "task step 2"
    
    cmd=>:
    echo "task step 2"
    -
    task step 2
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0089 log - verbose level v](../../logs/c0089_v)
* [c0089 log - verbose level vv](../../logs/c0089_vv)
* [c0089 log - verbose level vvv](../../logs/c0089_vvv)
* [c0089 log - verbose level vvvv](../../logs/c0089_vvvv)
* [c0089 log - verbose level vvvvv](../../logs/c0089_vvvvv)

##### References
* [Related Chapter](../../organization/c0089)
