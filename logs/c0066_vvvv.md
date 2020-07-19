---
title: "c0066_vvvv"
date: 2020-07-20T02:01:41+77:00
draft: false
weight: 10663

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0066
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0066
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
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    cmd( 1):
    echo "hello 1"
    
    cmd=>:
    echo "hello 1"<=
    hello 1
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "school": "Sydney Grammar"
    })
    
    ~SubStep1: [print: demo of print command ]
    hello, Sydney Grammar
    ~SubStep2: [reg: demo of reg command ]
    ~SubStep3: [print: show above reg var greet and it is available immediately in current func
    unlike the reg in template, it is available in the next step func execution
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    ~SubStep4: [reg: demo greetlocal is registered to local var only
    it is accessible in current func, but not next one
     ]
    ~SubStep5: [print: this show display a correct rendered value
     ]
    hello, hello, Sydney Grammar. registered to local func only
    -Step3: [: the greetlocal will not be availe in this func call ]
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    ~SubStep1: [print: this will show the registered global runtime var
     ]
    hello, <no value>
    ~SubStep2: [print: this will show <no value> for greetlocal, as it is not registered to global
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime"
    })
    
    ~SubStep1: [deReg: demo of deReg command ]
    deRegister var: greet
    -Step5: [: you will see that greet var is removed from global var map
    you will see <no value> here
     ]
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello {{.greet}}"
    
    cmd=>:
    echo "hello <no value>"<=
    hello <no value>
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0066 log - verbose level v](../../logs/c0066_v)
* [c0066 log - verbose level vv](../../logs/c0066_vv)
* [c0066 log - verbose level vvv](../../logs/c0066_vvv)
* [c0066 log - verbose level vvvv](../../logs/c0066_vvvv)
* [c0066 log - verbose level vvvvv](../../logs/c0066_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0066)
