---
title: "c0043_vvvv"
date: 2020-07-20T02:01:37+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0043
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
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
      })
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
      "b": "bb",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "a": "aa"
    })
    
    dvar> adebug:
    "aa"
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
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
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "c": "cc",
      "d": "dd"
    })
    
    dvar> cdebug:
    "cc"
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
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
