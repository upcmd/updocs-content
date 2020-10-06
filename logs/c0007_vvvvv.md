---
title: "c0007_vvvvv"
date: 2020-10-07T00:11:02+1010:00
draft: false
weight: 10074

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0007
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0007
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed0e0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0001308e8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
    cmd=>:
    echo "world"
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
    cmd=>:
    echo "world"
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\""
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
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "world"
    
    cmd=>:
    echo "world"
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0007 log - verbose level v](../../logs/c0007_v)
* [c0007 log - verbose level vv](../../logs/c0007_vv)
* [c0007 log - verbose level vvv](../../logs/c0007_vvv)
* [c0007 log - verbose level vvvv](../../logs/c0007_vvvv)
* [c0007 log - verbose level vvvvv](../../logs/c0007_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0007)
