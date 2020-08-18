---
title: "c0167_vvvv"
date: 2020-08-18T15:16:23+88:00
draft: false
weight: 11673

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0167
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
    loading [Task]:  ./tests/functests/c0167
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: demo varname to ref to a loop item from var ]
    current exec runtime vars:
    (*core.Cache)({
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    })
    
    ~SubStep1: [print:  ]
    item1
    ~SubStep1: [print:  ]
    item2
    ~SubStep1: [print:  ]
    item3
    -Step2: [: demo use dynamic key to ref to a loop item from var ]
    current exec runtime vars:
    (*core.Cache)({
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      }
    })
    
    ~SubStep1: [print:  ]
    item1
    ~SubStep1: [print:  ]
    item2
    ~SubStep1: [print:  ]
    item3
    
```

##### Logs with different verbose level
* [c0167 log - verbose level v](../../logs/c0167_v)
* [c0167 log - verbose level vv](../../logs/c0167_vv)
* [c0167 log - verbose level vvv](../../logs/c0167_vvv)
* [c0167 log - verbose level vvvv](../../logs/c0167_vvvv)
* [c0167 log - verbose level vvvvv](../../logs/c0167_vvvvv)

##### References
* [Related Chapter](../../loop/c0167)
