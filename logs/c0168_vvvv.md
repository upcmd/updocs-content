---
title: "c0168_vvvv"
date: 2020-09-18T01:27:52+99:00
draft: false
weight: 11683

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0168
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
    loading [Task]:  ./tests/functests/c0168
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
    
    -Step1: [: loopRange func will generate a range list named myloop
    myloop will be registered as local var
    the loop will use myloop to iterate through
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myloop": {
        1,
        2,
        3,
        4,
        5
      }
    })
    
    ~SubStep1: [print:  ]
    1
    ~SubStep1: [print:  ]
    2
    ~SubStep1: [print:  ]
    3
    ~SubStep1: [print:  ]
    4
    ~SubStep1: [print:  ]
    5
    -Step2: [: same as above, it will register a range list named my range
    myrange list's name is then returned from the func call in loopRange, then
    the name myrange will be used to refer to that var registered already
     ]
    current exec runtime vars:
    (*core.Cache)({
      "myloop": {
        1,
        2,
        3,
        4,
        5
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myloop": {
        1,
        2,
        3,
        4,
        5
      },
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    321
    ~SubStep1: [print:  ]
    322
    ~SubStep1: [print:  ]
    323
    ~SubStep1: [print:  ]
    324
    ~SubStep1: [print:  ]
    325
    ~SubStep1: [print:  ]
    326
    ~SubStep1: [print:  ]
    327
    ~SubStep1: [print:  ]
    328
    ~SubStep1: [print:  ]
    329
    ~SubStep1: [print:  ]
    330
    
```

##### Logs with different verbose level
* [c0168 log - verbose level v](../../logs/c0168_v)
* [c0168 log - verbose level vv](../../logs/c0168_vv)
* [c0168 log - verbose level vvv](../../logs/c0168_vvv)
* [c0168 log - verbose level vvvv](../../logs/c0168_vvvv)
* [c0168 log - verbose level vvvvv](../../logs/c0168_vvvvv)

##### References
* [Related Chapter](../../loop/c0168)
