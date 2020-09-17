---
title: "c0043_vvvv"
date: 2020-09-18T00:51:26+99:00
draft: false
weight: 10433

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0043
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
    loading [Task]:  ./tests/functests/c0043
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
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step3: [: this would be totally fine too without shell commands
    this step could be served as a intermediate step to
    register a var into global var map, and it will be
    avaiable after the next step
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "a": "aa",
      "b": "bb"
    })
    
    dvar> adebug:
    "aa"
    
    -
    aa
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "a": "aa",
      "b": "bb",
      "adebug": "aa"
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step4: [: in cmd, you can also do reg/deReg var in dvar evaluation
    the cmd func name makes more sense then shell func
    if you really want to do var manipulation only
     ]
    current exec runtime vars:
    (*core.Cache)({
      "d": "dd",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "c": "cc"
    })
    
    dvar> cdebug:
    "cc"
    
    -
    cc
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "c": "cc",
      "d": "dd",
      "cdebug": "cc"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    
```

##### Logs with different verbose level
* [c0043 log - verbose level v](../../logs/c0043_v)
* [c0043 log - verbose level vv](../../logs/c0043_vv)
* [c0043 log - verbose level vvv](../../logs/c0043_vvv)
* [c0043 log - verbose level vvvv](../../logs/c0043_vvvv)
* [c0043 log - verbose level vvvvv](../../logs/c0043_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0043)
