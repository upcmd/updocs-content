---
title: "c0192_vvvvv"
date: 2020-09-18T00:51:58+99:00
draft: false
weight: 11924

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0192
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
    loading [Task]:  ./tests/functests/c0192
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001db4e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "global_aa": "aa"
    }
    
    (core.Cache) (len=1) {
     (string) (len=9) "global_aa": (string) (len=2) "aa"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "global_aa": "aa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: loop through test cases ]
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": {
            "echo \"main task start\""
          }
        },
        {
          "func": "call",
          "do": "cc"
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "local_bb": "bb"
      },
      Dvars: {
        {
          Name: "task_tt",
          Value: "tt",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "loop through test cases",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "local_bb": "bb",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "task_tt": "tt"
    }
    
    
    scope[local] merged: {
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt",
      "global_aa": "aa"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"main task start\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "main task start"
    
    cmd=>:
    echo "main task start"
    -
    main task start
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"main task start\"",
     Code: (int) 0,
     Output: (string) (len=15) "main task start",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: "cc",
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
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb"
    })
    
    caller's vars to task (cc)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [cc]: 
    =Task2: [task ==> cc:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"in cc ....\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0
    })
    
    cmd( 1):
    echo "in cc ...."
    
    cmd=>:
    echo "in cc ...."
    -
    in cc ....
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"in cc ....\"",
     Code: (int) 0,
     Output: (string) (len=10) "in cc ....",
     ErrMsg: (string) ""
    }
    
    . ok
    task Finally:
    -Step1: [close_file: ensure the opened file is closed
     ]
    {
      Name: "close_file",
      Do: {
        "echo \"close the file {{.loopitem}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "finally_cc": "cc"
      },
      Dvars: <nil>,
      Desc: "ensure the opened file is closed\n",
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
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "finally_cc": "cc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "finally_cc": "cc",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "finally_cc": "cc",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt"
    })
    
    cmd( 1):
    echo "close the file {{.loopitem}}"
    
    cmd=>:
    echo "close the file item1"
    -
    close the file item1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"close the file item1\"",
     Code: (int) 0,
     Output: (string) (len=20) "close the file item1",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"main task start\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "local_bb": "bb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "local_bb": "bb",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "loopitem": "item2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "local_bb": "bb",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "loopitem": "item2"
    })
    
    cmd( 1):
    echo "main task start"
    
    cmd=>:
    echo "main task start"
    -
    main task start
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"main task start\"",
     Code: (int) 0,
     Output: (string) (len=15) "main task start",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: "cc",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1
    })
    
    caller's vars to task (cc)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2"
    })
    
      located task-> 2 [cc]: 
    =Task2: [task ==> cc:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"in cc ....\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
    cmd( 1):
    echo "in cc ...."
    
    cmd=>:
    echo "in cc ...."
    -
    in cc ....
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"in cc ....\"",
     Code: (int) 0,
     Output: (string) (len=10) "in cc ....",
     ErrMsg: (string) ""
    }
    
    . ok
    task Finally:
    -Step1: [close_file: ensure the opened file is closed
     ]
    {
      Name: "close_file",
      Do: {
        "echo \"close the file {{.loopitem}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "finally_cc": "cc"
      },
      Dvars: <nil>,
      Desc: "ensure the opened file is closed\n",
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
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "finally_cc": "cc",
      "loopitem": "item2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "finally_cc": "cc"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_bb": "bb",
      "finally_cc": "cc",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt"
    })
    
    cmd( 1):
    echo "close the file {{.loopitem}}"
    
    cmd=>:
    echo "close the file item2"
    -
    close the file item2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"close the file item2\"",
     Code: (int) 0,
     Output: (string) (len=20) "close the file item2",
     ErrMsg: (string) ""
    }
    
    . ok
    task Finally:
    Step1:
    {
      Name: "",
      Do: {
        "echo \"main task final\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "finally_task": "ff"
      },
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
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "finally_task": "ff"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "finally_task": "ff",
      "global_aa": "aa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "finally_task": "ff"
    })
    
    cmd( 1):
    echo "main task final"
    
    cmd=>:
    echo "main task final"
    -
    main task final
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"main task final\"",
     Code: (int) 0,
     Output: (string) (len=15) "main task final",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0192 log - verbose level v](../../logs/c0192_v)
* [c0192 log - verbose level vv](../../logs/c0192_vv)
* [c0192 log - verbose level vvv](../../logs/c0192_vvv)
* [c0192 log - verbose level vvvv](../../logs/c0192_vvvv)
* [c0192 log - verbose level vvvvv](../../logs/c0192_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0192)
