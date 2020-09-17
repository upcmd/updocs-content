---
title: "c0193_vvvvv"
date: 2020-09-18T01:27:59+99:00
draft: false
weight: 11934

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0193
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00024e140)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
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
    {
      Name: "",
      Do: "case3",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (case3)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 4 [case3]: 
    =Task4: [task ==> case3:  ]
    Executing task stack layer: 2
    
    --Step1: [: before sourcing, the env var: AAA does not exist
    this will cause an error
     ]
    {
      Name: "",
      Do: {
        "env |grep AAA"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "before sourcing, the env var: AAA does not exist\nthis will cause an error\n",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=13) "env |grep AAA",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step2: [: no source/srcfile input
    with name and action
    now it will save current shell env
    which has got no AAA in it
     ]
    {
      Name: "",
      Do: {
        {
          "name": "virtualEnv",
          "cmd": {
            "name": "venv0",
            "action": "snapshot"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "no source/srcfile input\nwith name and action\nnow it will save current shell env\nwhich has got no AAA in it\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
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
    
    map[action:snapshot name:venv0]
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step3: [: since there is no source, this will still cause an error
     ]
    {
      Name: "",
      Do: {
        "env |grep AAA"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "since there is no source, this will still cause an error\n",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=13) "env |grep AAA",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step4: [: now source and save current shell environment variables
     ]
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "name": "venv1",
            "action": "snapshot",
            "srcfile": "./tests/functests/test_env.rc"
          },
          "name": "virtualEnv"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "now source and save current shell environment variables\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
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
    
    map[action:snapshot name:venv1 srcfile:./tests/functests/test_env.rc]
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    start of source
    end of source
    
    --Step5: [: after sourcing, the env var: AAA exist
    the error should be cleared
     ]
    {
      Name: "",
      Do: {
        "env |grep AAA"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "after sourcing, the env var: AAA exist\nthe error should be cleared\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=13) "env |grep AAA",
     Code: (int) 0,
     Output: (string) (len=15) "AAA=sourced_aaa",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step6: [: now let's restore to the point of venv0
    which has got no AAA in it
     ]
    {
      Name: "",
      Do: {
        {
          "name": "virtualEnv",
          "cmd": {
            "name": "venv0",
            "action": "restore"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "now let's restore to the point of venv0\nwhich has got no AAA in it\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    }
    
    
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
    
    map[action:restore name:venv0]
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step7: [: this will still cause an error
    as now the shell env is restored to venv0
    which has got no AAA in it
     ]
    {
      Name: "",
      Do: {
        "env |grep AAA"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this will still cause an error\nas now the shell env is restored to venv0\nwhich has got no AAA in it\n",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 0,
        Output: "AAA=sourced_aaa",
        ErrMsg: ""
      })
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=13) "env |grep AAA",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step8: [: now let's restore to the point of venv1
    which has got AAA in it
    we expect the error is clear
     ]
    {
      Name: "",
      Do: {
        {
          "name": "virtualEnv",
          "cmd": {
            "name": "venv1",
            "action": "restore"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "now let's restore to the point of venv1\nwhich has got AAA in it\nwe expect the error is clear\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
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
    
    map[action:restore name:venv1]
    ~~SubStep1: [virtualEnv:  ]
    -sourcing execution result:
    
    --Step9: [: after sourcing, the env var: AAA exist
    the error should be cleared
     ]
    {
      Name: "",
      Do: {
        "env |grep AAA"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "after sourcing, the env var: AAA exist\nthe error should be cleared\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep AAA",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=13) "env |grep AAA",
     Code: (int) 0,
     Output: (string) (len=15) "AAA=sourced_aaa",
     ErrMsg: (string) ""
    }
    
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
