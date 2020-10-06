---
title: "c0011_vvvv"
date: 2020-10-06T23:45:52+1010:00
draft: false
weight: 10113

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0011
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
    loading [Task]:  ./tests/functests/c0011
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
      "b": "non-prod-b",
      "c": "non-prod-c",
      "a": "non-prod-a"
    })
    
    
    global: (*core.Cache)({
      "a": "global-a",
      "b": "global-b",
      "c": "global-c",
      "d": "global-d"
    })
    
    
    prod: (*core.Cache)({
      "a": "prod-a",
      "c": "prod-c"
    })
    
    
    groups members:[dr prod dev st staging]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "e": "runtime-e",
      "a": "runtime-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "k": "runtime-k"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "k": "runtime-k",
      "e": "runtime-e",
      "a": "runtime-a",
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
      "c": "dev-c",
      "up_runtime_task_layer_number": 0,
      "m": "local-m",
      "d": "global-d",
      "k": "runtime-k",
      "e": "local-e",
      "a": "runtime-a",
      "b": "non-prod-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "dev-c",
      "up_runtime_task_layer_number": 0,
      "m": "local-m",
      "d": "global-d",
      "k": "runtime-k",
      "e": "local-e",
      "a": "runtime-a",
      "b": "non-prod-b"
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
* [c0011 log - verbose level v](../../logs/c0011_v)
* [c0011 log - verbose level vv](../../logs/c0011_vv)
* [c0011 log - verbose level vvv](../../logs/c0011_vvv)
* [c0011 log - verbose level vvvv](../../logs/c0011_vvvv)
* [c0011 log - verbose level vvvvv](../../logs/c0011_vvvvv)

##### References
* [Related Chapter](../../scope/c0011)
