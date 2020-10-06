---
title: "c0122_vvvv"
date: 2020-10-07T00:11:21+1010:00
draft: false
weight: 11223

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0122
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
    loading [Task]:  ./tests/functests/c0122
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    tom
    ~SubStep2: [print:  ]
    None
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    hello tom
    -Step3: [: add support if the element does not exist, then if condition should be false by default ]
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_age": ".student.age",
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0122 log - verbose level v](../../logs/c0122_v)
* [c0122 log - verbose level vv](../../logs/c0122_vv)
* [c0122 log - verbose level vvv](../../logs/c0122_vvv)
* [c0122 log - verbose level vvvv](../../logs/c0122_vvvv)
* [c0122 log - verbose level vvvvv](../../logs/c0122_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0122)
