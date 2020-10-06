---
title: "c0150_vvvvv"
date: 2020-10-07T00:11:27+1010:00
draft: false
weight: 11504

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0150
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
    loading [Task]:  ./tests/functests/c0150
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000c49a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000a0110)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 3 [task]: 
    Task3: [task ==> task: build the showcases automatically ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "facts",
        "testingWarning"
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
    
    caller's vars to task (facts)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 1 [facts]: 
    =Task1: [task ==> facts: gather facts ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "uname"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "result",
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
    uname
    
    cmd=>:
    uname
    -
    Linux
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=5) "uname",
     Code: (int) 0,
     Output: (string) (len=5) "Linux",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step2: [: get os  - [Darwin | Linux] ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "facts OS: {{.os}}"
        },
        {
          "name": "return",
          "cmd": {
            "os"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "os",
          Value: "{{ .result.Output }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
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
      Desc: "get os  - [Darwin | Linux]",
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
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    dvar> os:
    "Linux"
    
    -
    Linux
    [local] dvar expanded result:
    {
      "os": "Linux"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux",
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      })
    })
    
    facts OS: {{.os}}
    ~~SubStep1: [print:  ]
    facts OS: Linux
    [os]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "os": "Linux"
    })
    
    caller's vars to task (testingWarning)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux"
    })
    
      located task-> 2 [testingWarning]: 
    =Task2: [task ==> testingWarning: it should warn if the build task is for testing only ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "in sub task - building OS: {{.os}}"
            },
            {
              "name": "colorPrint",
              "cmd": {
                "msg": "?? WARN - This is a build for testing purpose only",
                "fg": "red"
              }
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{ eq .os \"Darwin\" }}",
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
      "os": "Linux",
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "uname",
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux"
    })
    
    condition failed, skip executing step 
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "cmd": "in main task - building OS: {{.os}}",
          "name": "print"
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
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    in main task - building OS: {{.os}}
    ~SubStep1: [print:  ]
    in main task - building OS: Linux
    
```

##### Logs with different verbose level
* [c0150 log - verbose level v](../../logs/c0150_v)
* [c0150 log - verbose level vv](../../logs/c0150_vv)
* [c0150 log - verbose level vvv](../../logs/c0150_vvv)
* [c0150 log - verbose level vvvv](../../logs/c0150_vvvv)
* [c0150 log - verbose level vvvvv](../../logs/c0150_vvvvv)

##### References
* [Related Chapter](../../call-func/c0150)
