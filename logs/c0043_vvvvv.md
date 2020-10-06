---
title: "c0043_vvvvv"
date: 2020-10-06T23:45:58+1010:00
draft: false
weight: 10434

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0043
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
    loading [Task]:  ./tests/functests/c0043
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef220)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0001308f0)({
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
    
    . ok
    -Step2:
    {
      Name: "",
      Do: <nil>,
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
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step3: [
    this would be totally fine too without shell commands
    this step could be served as a intermediate step to
    register a var into global var map, and it will be
    avaiable after the next step
    ]
    {
      Name: "",
      Do: <nil>,
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "aa",
        "b": "bb"
      },
      Dvars: {
        {
          Name: "adebug",
          Value: "{{.a}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
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
      Desc: "this would be totally fine too without shell commands\nthis step could be served as a intermediate step to\nregister a var into global var map, and it will be\navaiable after the next step\n",
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
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "a": "aa",
      "b": "bb"
    })
    
    dvar> adebug:
    "aa"
    
    -
    aa
    [local] dvar expanded result:
    {
      "adebug": "aa"
    }
    
    
    scope[local] merged: {
      "adebug": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "a": "aa",
      "b": "bb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "a": "aa",
      "b": "bb",
      "adebug": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step4: [
    in cmd, you can also do reg/deReg var in dvar evaluation
    the cmd func name makes more sense then shell func
    if you really want to do var manipulation only
    ]
    {
      Name: "",
      Do: <nil>,
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "c": "cc",
        "d": "dd"
      },
      Dvars: {
        {
          Name: "cdebug",
          Value: "{{.c}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
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
      Desc: "in cmd, you can also do reg/deReg var in dvar evaluation\nthe cmd func name makes more sense then shell func\nif you really want to do var manipulation only\n",
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
      "c": "cc",
      "d": "dd",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    dvar> cdebug:
    "cc"
    
    -
    cc
    [local] dvar expanded result:
    {
      "cdebug": "cc"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "c": "cc",
      "d": "dd",
      "cdebug": "cc"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "c": "cc",
      "d": "dd",
      "cdebug": "cc",
      "last_result": (*utils.ExecResult)({
        Cmd: "",
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    
```

##### Logs with different verbose level
* [c0043 log - verbose level v](../../logs/c0043_v)
* [c0043 log - verbose level vv](../../logs/c0043_vv)
* [c0043 log - verbose level vvv](../../logs/c0043_vvv)
* [c0043 log - verbose level vvvv](../../logs/c0043_vvvv)
* [c0043 log - verbose level vvvvv](../../logs/c0043_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0043)
