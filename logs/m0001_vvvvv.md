---
title: "0001_vvvvv"
date: 2020-07-20T02:02:14+77:00
draft: false
weight: 100104

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0001/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0001
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0001
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0001
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc00026efa0)(<nil>)
    
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
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: main job ]
    {
      Name: "",
      Do: {
        "echo \"hello world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "main job",
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
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello world"
    
    cmd=>:
    echo "hello world"<=
    hello world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello world\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: "internal_task",
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (internal_task)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    this is a internal task
    ~~SubStep1: [print:  ]
    this is a internal task
    -Step3:
    {
      Name: "",
      Do: "hello-module.Say_world",
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000a0640)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [hello-module] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
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
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "... world"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "aaa"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "a": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ... world
    ~SubStep1: [print:  ]
    ... world
    
```

##### Logs with different verbose level
* [m0001 log - verbose level v](../../logs/m0001_v)
* [m0001 log - verbose level vv](../../logs/m0001_vv)
* [m0001 log - verbose level vvv](../../logs/m0001_vvv)
* [m0001 log - verbose level vvvv](../../logs/m0001_vvvv)
* [m0001 log - verbose level vvvvv](../../logs/m0001_vvvvv)

##### References
* [Related Chapter](../../module/0001)
