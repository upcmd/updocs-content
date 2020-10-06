---
title: "c0123_vvvv"
date: 2020-10-07T00:11:22+1010:00
draft: false
weight: 11233

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0123
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
    loading [Task]:  ./tests/functests/c0123
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
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
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
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
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
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    hello tom
    -Step3: [: add support if the element does not exist, then if condition should be false by default ]
    current exec runtime vars:
    (*core.Cache)({
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "tom",
        "sex": "male"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    -Step4: [query:  ]
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "tom",
        "sex": "male"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "sex": "male",
        "name": "tom"
      },
      "ymldoc": "student:\n  name: tom\n  sex: male\n",
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0123 log - verbose level v](../../logs/c0123_v)
* [c0123 log - verbose level vv](../../logs/c0123_vv)
* [c0123 log - verbose level vvv](../../logs/c0123_vvv)
* [c0123 log - verbose level vvvv](../../logs/c0123_vvvv)
* [c0123 log - verbose level vvvvv](../../logs/c0123_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0123)
