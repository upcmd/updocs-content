---
title: "c0005_vvvvv"
date: 2020-07-01T15:34:21+77:00
draft: false
weight: 10054

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0005
                 Verbose -> vvvvv
              ModuleName -> tender_stallman0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0005
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001853c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [tender_stallman0] instance id: [dev]
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
    
      located task-> 4 [task]: 
    Task4: [task ==> task: this is the task and expect the final message (hello I love this world) ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "pre_task",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (pre_task)::
    (*core.Cache)({
    })
    
      located task-> 1 [pre_task]: 
    =Task1: [task ==> pre_task: this is pre-task ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"hello\""
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
      VarsFile: ""
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
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \" I love this \""
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
      VarsFile: ""
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
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo " I love this "
    
     \_ echo " I love this "
    I love this
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "I love this",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "post_task",
        "2ndtask"
      },
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (post_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [post_task]: 
    =Task2: [task ==> post_task: this is post-task ]
    Executing task stack layer: 2
    
    --Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do step1 in shell func",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (2ndtask)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [2ndtask]: 
    =Task3: [task ==> 2ndtask:  ]
    Executing task stack layer: 2
    
    --Step1: [: to test multiple refs ]
    {
      Name: "",
      Do: {
        "echo \"this is 2nd task\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "to test multiple refs",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    tender_stallman0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "this is 2nd task"
    
     \_ echo "this is 2nd task"
    this is 2nd task
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=16) "this is 2nd task",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0005 log - verbose level v](../../logs/c0005_v)
* [c0005 log - verbose level vv](../../logs/c0005_vv)
* [c0005 log - verbose level vvv](../../logs/c0005_vvv)
* [c0005 log - verbose level vvvv](../../logs/c0005_vvvv)
* [c0005 log - verbose level vvvvv](../../logs/c0005_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0005)
