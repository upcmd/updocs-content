---
title: "c0157_vvvv"
date: 2020-08-09T01:36:23+88:00
draft: false
weight: 11573

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0157
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
    loading [Task]:  ./tests/functests/c0157
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
      "person": {
        "name": "tom"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "person": {
        "name": "tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: the commented if statement will cause a template rendering issue since person.school is not able to be determined
     ]
    current exec runtime vars:
    (*core.Cache)({
      "person": {
        "name": "tom"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom"
      }
    })
    
    ~SubStep1: [print:  ]
    hello: tom
    -Step2: [: correct way is to try to get the school value and save it to a dvar
    then it is deterministic of the school value
     ]
    current exec runtime vars:
    (*core.Cache)({
      "person": {
        "name": "tom"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom"
      },
      "school": "None"
    })
    
    ~SubStep1: [print:  ]
    hello: tom
    
```

##### Logs with different verbose level
* [c0157 log - verbose level v](../../logs/c0157_v)
* [c0157 log - verbose level vv](../../logs/c0157_vv)
* [c0157 log - verbose level vvv](../../logs/c0157_vvv)
* [c0157 log - verbose level vvvv](../../logs/c0157_vvvv)
* [c0157 log - verbose level vvvvv](../../logs/c0157_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0157)
