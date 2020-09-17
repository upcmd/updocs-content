---
title: "c0131_vvvvv"
date: 2020-09-18T00:51:45+99:00
draft: false
weight: 11314

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0131
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
    loading [Task]:  ./tests/functests/c0131
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175560)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "goahead": false
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "goahead": (bool) false
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "goahead": false
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "true/false value of goahead:\n{{.goahead}}\n{{not .goahead}}\n"
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
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    true/false value of goahead:
    {{.goahead}}
    {{not .goahead}}
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
    true
    
    -Step2: [: show use a flow in else ]
    {
      Name: "",
      Do: {
        "goahead"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "show use a flow in else",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "do something else step1 ......."
            }
          }
        },
        {
          "func": "shell",
          "do": {
            "echo do something else step2 ......."
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "do something else step3 ......."
            }
          }
        },
        {
          "desc": "show it is same that you could assemble a list of tasks for if true condition",
          "vars": {
            "goahead": true
          },
          "do": {
            "goelse"
          },
          "func": "call"
        }
      },
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
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "goahead": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else step1 ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    do something else step1 .......
    ~SubStep1: [print:  ]
    do something else step1 .......
    -Step2:
    {
      Name: "",
      Do: {
        "echo do something else step2 ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo do something else step2 .......
    
    cmd=>:
    echo do something else step2 .......
    -
    do something else step2 .......
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=36) "echo do something else step2 .......",
     Code: (int) 0,
     Output: (string) (len=31) "do something else step2 .......",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else step3 ......."
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
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    do something else step3 .......
    ~SubStep1: [print:  ]
    do something else step3 .......
    -Step4: [: show it is same that you could assemble a list of tasks for if true condition ]
    {
      Name: "",
      Do: {
        "goelse"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "goahead": true
      },
      Dvars: <nil>,
      Desc: "show it is same that you could assemble a list of tasks for if true condition",
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
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (goelse)::
    (*core.Cache)({
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else ......."
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
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      })
    })
    
    do something else .......
    ~~SubStep1: [print:  ]
    do something else .......
    
```

##### Logs with different verbose level
* [c0131 log - verbose level v](../../logs/c0131_v)
* [c0131 log - verbose level vv](../../logs/c0131_vv)
* [c0131 log - verbose level vvv](../../logs/c0131_vvv)
* [c0131 log - verbose level vvvv](../../logs/c0131_vvvv)
* [c0131 log - verbose level vvvvv](../../logs/c0131_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0131)
