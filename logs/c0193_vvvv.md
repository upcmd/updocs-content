---
title: "c0193_vvvv"
date: 2020-09-18T00:51:58+99:00
draft: false
weight: 11933

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0193
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
    loading [Task]:  ./tests/functests/c0193
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
    Task1: [task ==> task: please switch to use case1|case2 ...
    the reason we do not chain all cases together is because
    the venv will pollute the entire running session unless you mananage to restore it
     ]
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
    
      located task-> 4 [case3]: 
    =Task4: [task ==> case3:  ]
    Executing task stack layer: 2
    
    --Step1: [: before sourcing, the env var: AAA does not exist
    this will cause an error
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    env |grep AAA
    
    cmd=>:
    env |grep AAA
    -
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step2: [: no source/srcfile input
    with name and action
    now it will save current shell env
    which has got no AAA in it
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step3: [: since there is no source, this will still cause an error
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    env |grep AAA
    
    cmd=>:
    env |grep AAA
    -
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step4: [: now source and save current shell environment variables
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    start of source
    end of source
    
    --Step5: [: after sourcing, the env var: AAA exist
    the error should be cleared
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    cmd( 1):
    env |grep AAA
    
    cmd=>:
    env |grep AAA
    -
    AAA=sourced_aaa
    
    -
     .. ok
    . ok
    --Step6: [: now let's restore to the point of venv0
    which has got no AAA in it
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step7: [: this will still cause an error
    as now the shell env is restored to venv0
    which has got no AAA in it
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    env |grep AAA
    
    cmd=>:
    env |grep AAA
    -
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step8: [: now let's restore to the point of venv1
    which has got AAA in it
    we expect the error is clear
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step9: [: after sourcing, the env var: AAA exist
    the error should be cleared
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    cmd( 1):
    env |grep AAA
    
    cmd=>:
    env |grep AAA
    -
    AAA=sourced_aaa
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0193 log - verbose level v](../../logs/c0193_v)
* [c0193 log - verbose level vv](../../logs/c0193_vv)
* [c0193 log - verbose level vvv](../../logs/c0193_vvv)
* [c0193 log - verbose level vvvv](../../logs/c0193_vvvv)
* [c0193 log - verbose level vvvvv](../../logs/c0193_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0193)
