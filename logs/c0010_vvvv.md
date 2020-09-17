---
title: "c0010_vvvv"
date: 2020-09-18T00:51:20+99:00
draft: false
weight: 10103

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0010
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0010
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
      "c": {
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c1": "nonprod-c1",
        "c2": "nonprod-c2",
        "c3": {
          "c33": "nonprod-c33",
          "c32": "nonprod-c32"
        }
      },
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
    
    global: {
      "b": "global-b",
      "c": {
        "c2": "global-c2",
        "c3": {
          "c32": "global-c32",
          "c33": "global-c33",
          "c31": "global-c31"
        },
        "c4": "global-c4",
        "c1": "global-c1"
      },
      "d": "global-d",
      "a": "global-a"
    }
    
    
    groups members:[dr prod dev st staging]
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c7": "dev-c7",
        "c1": "dev-c1",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        },
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c6": "dev-c6"
      },
      "d": "global-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": {
        "c7": "dev-c7",
        "c1": "dev-c1",
        "c2": "dev-c2",
        "c3": {
          "c31": "global-c31",
          "c32": "nonprod-c32",
          "c33": "dev-c33"
        },
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c6": "dev-c6"
      },
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c1": "dev-c1",
        "c2": "dev-c2",
        "c3": {
          "c33": "dev-c33",
          "c31": "global-c31",
          "c32": "nonprod-c32"
        },
        "c4": "nonprod-c4",
        "c5": "nonprod-c5"
      },
      "d": "global-d",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c1": "dev-c1",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        }
      },
      "d": "global-d",
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
* [c0010 log - verbose level v](../../logs/c0010_v)
* [c0010 log - verbose level vv](../../logs/c0010_vv)
* [c0010 log - verbose level vvv](../../logs/c0010_vvv)
* [c0010 log - verbose level vvvv](../../logs/c0010_vvvv)
* [c0010 log - verbose level vvvvv](../../logs/c0010_vvvvv)

##### References
* [Related Chapter](../../scope/c0010)
