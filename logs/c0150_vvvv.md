---
title: "c0150_vvvv"
date: 2020-08-18T15:16:19+88:00
draft: false
weight: 11503

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0150
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
    loading [Task]:  ./tests/functests/c0150
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
    
      located task-> 3 [task]: 
    Task3: [task ==> task: build the showcases automatically ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
      located task-> 1 [facts]: 
    =Task1: [task ==> facts: gather facts ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    uname
    
    cmd=>:
    uname
    -
    Linux
    -
     .. ok
    . ok
    --Step2: [: get os  - [Darwin | Linux] ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      })
    })
    
    dvar> os:
    "Linux"
    
    -
    Linux
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "os": "Linux",
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    facts OS: Linux
    ~~SubStep2: [return:  ]
      located task-> 2 [testingWarning]: 
    =Task2: [task ==> testingWarning: it should warn if the build task is for testing only ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [print:  ]
    in main task - building OS: Linux
    
```

##### Logs with different verbose level
* [c0150 log - verbose level v](../../logs/c0150_v)
* [c0150 log - verbose level vv](../../logs/c0150_vv)
* [c0150 log - verbose level vvv](../../logs/c0150_vvv)
* [c0150 log - verbose level vvvv](../../logs/c0150_vvvv)
* [c0150 log - verbose level vvvvv](../../logs/c0150_vvvvv)

##### References
* [Related Chapter](../../call-func/c0150)
