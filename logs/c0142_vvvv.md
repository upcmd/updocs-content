---
title: "c0142_vvvv"
date: 2020-08-09T01:36:20+88:00
draft: false
weight: 11423

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0142
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
    loading [Task]:  ./tests/functests/c0142
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
      "objectname": "person",
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "objectname": "person",
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    ~SubStep1: [colorPrint:  ]
    37 44
    hello, world
    ~SubStep2: [colorPrint:  ]
    37 44
    hello, world
    ~SubStep3: [colorPrint:  ]
    37 44
    hello, world
    ~SubStep4: [colorPrint:  ]
    37 44
    hello, world
    ~SubStep5: [colorPrint:  ]
    37 44
    tom: 18
    ~SubStep6: [colorPrint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    ~SubStep7: [colorPrint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    ~SubStep8: [colorPrint:  ]
    37 44
     WARN: [colorPrint] - [msg and object can not coexist]
    
```

##### Logs with different verbose level
* [c0142 log - verbose level v](../../logs/c0142_v)
* [c0142 log - verbose level vv](../../logs/c0142_vv)
* [c0142 log - verbose level vvv](../../logs/c0142_vvv)
* [c0142 log - verbose level vvvv](../../logs/c0142_vvvv)
* [c0142 log - verbose level vvvvv](../../logs/c0142_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0142)
