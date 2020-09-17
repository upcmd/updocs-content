---
title: "c0066_vvvv"
date: 2020-09-18T01:27:31+99:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0066
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
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
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello 1"
    
    cmd=>:
    echo "hello 1"
    -
    hello 1
    
    -
     .. ok
    . ok
    -Step2:
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
      "up_runtime_task_layer_number": 0
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
      "up_runtime_task_layer_number": 0,
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
    
    ~SubStep1: [print: this will show the registered global runtime var
     ]
    hello, <no value>
    ~SubStep2: [print: this will show <no value> for greetlocal, as it is not registered to global
     ]
    hello, from local dvars, Sydney Grammar. registered to global runtime
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "up_runtime_task_layer_number": 0,
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
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet": "from local dvars, Sydney Grammar. registered to global runtime",
      "up_runtime_task_layer_number": 0,
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
    
    ~SubStep1: [deReg: demo of deReg command ]
    deRegister var: greet
    -Step5: [: you will see that greet var is removed from global var map
    you will see <no value> here
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello {{.greet}}"
    
    cmd=>:
    echo "hello <no value>"
    -
    hello <no value>
    
    -
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
