---
title: "c0179_vvvvv"
date: 2020-10-07T00:11:32+1010:00
draft: false
weight: 11794

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0179
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
    loading [Task]:  ./tests/functests/c0179
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002966c0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0002b20e8)({
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
      Do: "echo hello",
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
    echo hello
    
    cmd=>:
    echo hello
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hello",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.last_result.Output}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    {{.last_result.Output}}
    ~SubStep1: [print:  ]
    hello
    -Step3:
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": "echo world"
        },
        {
          "do": {
            {
              "name": "print",
              "cmd": "{{.last_result.Output}}"
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .last_result.Output \"world\" }}"
              }
            }
          },
          "func": "cmd"
        }
      },
      Dox: <nil>,
      Func: "block",
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
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hello",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    -Step1:
    {
      Name: "",
      Do: "echo world",
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
    echo world
    
    cmd=>:
    echo world
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo world",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.last_result.Output}}"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .last_result.Output \"world\" }}"
          }
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
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
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    {{.last_result.Output}}
    ~SubStep1: [print:  ]
    world
    [{{eq .last_result.Output "world" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .last_result.Output "world" }}]
    -Step4: [: after the block func call ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.last_result.Output}}"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .last_result.Output \"world\" }}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "after the block func call",
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
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    {{.last_result.Output}}
    ~SubStep1: [print:  ]
    world
    [{{eq .last_result.Output "world" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .last_result.Output "world" }}]
    
```

##### Logs with different verbose level
* [c0179 log - verbose level v](../../logs/c0179_v)
* [c0179 log - verbose level vv](../../logs/c0179_vv)
* [c0179 log - verbose level vvv](../../logs/c0179_vvv)
* [c0179 log - verbose level vvvv](../../logs/c0179_vvvv)
* [c0179 log - verbose level vvvvv](../../logs/c0179_vvvvv)

##### References
* [Related Chapter](../../error_handling/c0179)
