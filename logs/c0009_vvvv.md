---
title: "c0009_vvvv"
date: 2020-07-20T02:01:30+77:00
draft: false
weight: 10093

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0009
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0009
    loading [ref vars]:  ./tests/functests/d0009-global.yml
    loading vars from: d0009-global.yml
    
    {
      "a": "global-a",
      "b": "global-b",
      "c": "global-c",
      "d": "global-d"
    }
    
    loading [ref vars]:  ./tests/functests/d0009-dev.yml
    loading vars from: d0009-dev.yml
    
    {
      "a": "dev-a",
      "c": "dev-c"
    }
    
    ---------group vars----------
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
    
    global: {
      "d": "global-d",
      "a": "global-a",
      "b": "global-b",
      "c": "global-c"
    }
    
    
    prod: {
      "c": "prod-c",
      "a": "prod-a"
    }
    
    
    groups members:[dr prod dev st staging]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
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
* [c0009 log - verbose level v](../../logs/c0009_v)
* [c0009 log - verbose level vv](../../logs/c0009_vv)
* [c0009 log - verbose level vvv](../../logs/c0009_vvv)
* [c0009 log - verbose level vvvv](../../logs/c0009_vvvv)
* [c0009 log - verbose level vvvvv](../../logs/c0009_vvvvv)

##### References
* [Related Chapter](../../scope/c0009)
