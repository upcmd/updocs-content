---
title: "c0104_vvvvv"
date: 2020-07-20T02:01:48+77:00
draft: false
weight: 11044

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0104
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0104
    -------full vars in scopes------
    (*impl.Scopes)(0xc000235400)(<nil>)
    
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
      "extra_task_name": "post_task"
    }
    
    (core.Cache) (len=1) {
     (string) (len=15) "extra_task_name": (string) (len=9) "post_task"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "extra_task_name": "post_task"
    }
    
      located task-> 4 [task]: 
    Task4: [task ==> task: this is the task and expect the final message (hello I love this world) ]
    Executing task stack layer: 1
    
    -Step1:
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
      "extra_task_name": "post_task"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "extra_task_name": "post_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task"
    })
    
    cmd( 1):
    echo " I love this "
    
    cmd=>:
    echo " I love this "<=
    I love this
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \" I love this \"",
     Code: (int) 0,
     Output: (string) (len=11) "I love this",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: use a dynamic var to refer to a task name ]
    {
      Name: "",
      Do: {
        "{{.extra_task_name}}",
        "2ndtask"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "use a dynamic var to refer to a task name",
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "extra_task_name": "post_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (post_task)::
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
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
      "up_runtime_task_layer_number": 1,
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "world"
    
    cmd=>:
    echo "world"<=
    world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (2ndtask)::
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
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
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "this is 2nd task"
    
    cmd=>:
    echo "this is 2nd task"<=
    this is 2nd task
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=23) "echo \"this is 2nd task\"",
     Code: (int) 0,
     Output: (string) (len=16) "this is 2nd task",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0104 log - verbose level v](../../logs/c0104_v)
* [c0104 log - verbose level vv](../../logs/c0104_vv)
* [c0104 log - verbose level vvv](../../logs/c0104_vvv)
* [c0104 log - verbose level vvvv](../../logs/c0104_vvvv)
* [c0104 log - verbose level vvvvv](../../logs/c0104_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0104)
