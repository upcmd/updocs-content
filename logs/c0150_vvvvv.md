---
title: "c0150_vvvvv"
date: 2020-07-01T15:34:43+77:00
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
              ModuleName -> tender_shockley0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0150
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001d55a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [tender_shockley0] instance id: [dev]
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
    
    
    tender_shockley0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (facts)::
    (*core.Cache)({
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
    
    
    tender_shockley0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    uname
    
     \_ uname
    Linux
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    dvar> os:
    "Linux"
    
    [local] dvar expanded result:
    {
      "os": "Linux"
    }
    
    
    scope[local] merged: {
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "os": "Linux"
    }
    
    
    tender_shockley0: overall final exec vars:
    
    (*core.Cache)({
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "os": "Linux"
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
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
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
          "do": {
            {
              "name": "print",
              "cmd": "in sub task - building OS: {{.os}}"
            },
            {
              "name": "colorprint",
              "cmd": {
                "msg": "?? WARN - This is a build for testing purpose only",
                "fg": "red"
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
      If: "{{ eq .os \"Darwin\" }}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux"
    }
    
    
    tender_shockley0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      }),
      "os": "Linux",
      "up_runtime_task_layer_number": 1,
      "result": (*utils.ExecResult)({
        Code: 0,
        Output: "Linux",
        ErrMsg: ""
      })
    })
    
    condition failed, skip executing step 
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in main task - building OS: {{.os}}"
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
    
    
    tender_shockley0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "os": "Linux"
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
