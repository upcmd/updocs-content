---
title: "c0011_vvvv"
date: 2020-08-09T01:36:00+88:00
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
    
    prod: {
      "c": "prod-c",
      "a": "prod-a"
    }
    
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
    
    global: {
      "c": "global-c",
      "d": "global-d",
      "a": "global-a",
      "b": "global-b"
    }
    
    
    groups members:[dr prod dev st staging]
    merged[ dev ] runtime vars:
    {
      "a": "runtime-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "d": "global-d",
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a",
      "b": "non-prod-b",
      "c": "dev-c"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "runtime-a",
      "b": "non-prod-b",
      "m": "local-m",
      "c": "dev-c",
      "d": "global-d",
      "e": "local-e",
      "k": "runtime-k"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "e": "local-e",
      "k": "runtime-k",
      "a": "runtime-a",
      "b": "non-prod-b",
      "m": "local-m",
      "c": "dev-c",
      "d": "global-d"
    })
    
    cmd( 1):
    echo "test out the var scopes only"
    
    cmd=>:
    echo "test out the var scopes only"<=
    test out the var scopes only
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
