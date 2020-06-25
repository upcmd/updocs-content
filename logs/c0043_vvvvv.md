---
title: "c0043_vvvvv"
date: 2020-06-25T01:55:44+66:00
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
              ModuleName -> fervent_swartz8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0043
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f5140)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [fervent_swartz8] instance id: [dev]
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
    
    
    fervent_swartz8: overall final exec vars:
    
    (*core.Cache)({
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    }
    
    
    fervent_swartz8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step3: [: this would be totally fine too without shell commands
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "aa",
      "b": "bb",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    dvar> adebug:
    "aa"
    
    [local] dvar expanded result:
    {
      "adebug": "aa"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "a": "aa",
      "b": "bb",
      "adebug": "aa"
    }
    
    
    fervent_swartz8: overall final exec vars:
    
    (*core.Cache)({
      "b": "bb",
      "adebug": "aa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "a": "aa"
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    -Step4: [: in cmd, you can also do reg/dereg var in dvar evaluation
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
      Desc: "in cmd, you can also do reg/dereg var in dvar evaluation\nthe cmd func name makes more sense then shell func\nif you really want to do var manipulation only\n",
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
      "c": "cc",
      "d": "dd",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    dvar> cdebug:
    "cc"
    
    [local] dvar expanded result:
    {
      "cdebug": "cc"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "c": "cc",
      "d": "dd",
      "cdebug": "cc"
    }
    
    
    fervent_swartz8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "c": "cc",
      "d": "dd",
      "cdebug": "cc"
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