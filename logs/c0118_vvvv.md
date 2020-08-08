---
title: "c0118_vvvv"
date: 2020-08-09T01:36:16+88:00
draft: false
weight: 11183

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0118
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
    loading [Task]:  ./tests/functests/c0118
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
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "loopkey": "items"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [step1: demo loop will not be executed if false ]
    current exec runtime vars:
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "person": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "person": "tom"
    })
    
    condition failed, skip executing step step1
    
    -Step2: [step1: demo use if condition is true ]
    current exec runtime vars:
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "person": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      },
      "person": "tom"
    })
    
    condition failed, skip executing step step1
    
    -Step3: [step1: demo use dynamic key to ref to a loop item from var ]
    current exec runtime vars:
    (*core.Cache)({
      "loopkey": "items",
      "items": {
        "item1",
        "item2",
        "item3"
      }
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
* [c0118 log - verbose level v](../../logs/c0118_v)
* [c0118 log - verbose level vv](../../logs/c0118_vv)
* [c0118 log - verbose level vvv](../../logs/c0118_vvv)
* [c0118 log - verbose level vvvv](../../logs/c0118_vvvv)
* [c0118 log - verbose level vvvvv](../../logs/c0118_vvvvv)

##### References
* [Related Chapter](../../loop/c0118)
