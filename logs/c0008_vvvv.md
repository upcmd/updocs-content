---
title: "c0008_vvvv"
date: 2020-10-07T00:11:02+1010:00
draft: false
weight: 10083

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0008
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
    loading [Task]:  ./tests/functests/c0008
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    prod: (*core.Cache)({
      "a": "prod-a",
      "c": "prod-c"
    })
    
    
    nonprod: (*core.Cache)({
      "c": "non-prod-c",
      "a": "non-prod-a",
      "b": "non-prod-b"
    })
    
    
    global: (*core.Cache)({
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    })
    
    
    groups members:[dr prod dev st staging]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "test out the var scopes only"
    
    cmd=>:
    echo "test out the var scopes only"
    -
    test out the var scopes only
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0008 log - verbose level v](../../logs/c0008_v)
* [c0008 log - verbose level vv](../../logs/c0008_vv)
* [c0008 log - verbose level vvv](../../logs/c0008_vvv)
* [c0008 log - verbose level vvvv](../../logs/c0008_vvvv)
* [c0008 log - verbose level vvvvv](../../logs/c0008_vvvvv)

##### References
* [Related Chapter](../../scope/c0008)
