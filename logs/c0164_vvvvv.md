---
title: "c0164_vvvvv"
date: 2020-10-07T00:11:30+1010:00
draft: false
weight: 11644

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0164
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
    loading [Task]:  ./tests/functests/c0164
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f7660)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b6920)({
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
      Do: <nil>,
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "aaa",
          Value: "var_a_from_task",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "countries",
          Value: "- Austraila\n- US\n- China\n- Japan\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "toObj",
            "keepName",
            "taskScope",
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
    
    dvar> countries:
    "- Austraila\n- US\n- China\n- Japan\n"
    
    -
    - Austraila
    - US
    - China
    - Japan
    
    dvar[object]> countries:
    {
      "Austraila",
      "US",
      "China",
      "Japan"
    }
    
    [local] dvar expanded result:
    {
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.countries}}"
        },
        {
          "name": "typeOf",
          "cmd": {
            "countries"
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
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    {{.countries}}
    ~SubStep1: [print:  ]
    [Austraila US China Japan]
    [countries]
    ~SubStep2: [typeOf:  ]
     1 -  type of [countries] > [[]interface {}]
    -Step3:
    {
      Name: "",
      Do: {
        "sub_task"
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
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "desc": "inspect if the correct parameter has been passed in correctly\nwith default value\nin block func\n",
          "do": {
            {
              "cmd": {
                "{{eq .aaa \"var_a_from_task\"}}"
              },
              "name": "assert"
            }
          }
        },
        {
          "func": "shell",
          "do": {
            "echo \"{{.aaa}}\"",
            "echo \"{{.loopitem}}\""
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "aaa": "var_a_from_sub_task"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: "countries",
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task"
    })
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .aaa \"var_a_from_task\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwith default value\nin block func\n",
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
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"{{.aaa}}\"",
        "echo \"{{.loopitem}}\""
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
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"var_a_from_task\"",
     Code: (int) 0,
     Output: (string) (len=15) "var_a_from_task",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Austraila"
    -
    Austraila
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"Austraila\"",
     Code: (int) 0,
     Output: (string) (len=9) "Austraila",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .aaa \"var_a_from_task\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwith default value\nin block func\n",
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
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US"
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"{{.aaa}}\"",
        "echo \"{{.loopitem}}\""
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"var_a_from_task\"",
     Code: (int) 0,
     Output: (string) (len=15) "var_a_from_task",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "US"
    -
    US
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=9) "echo \"US\"",
     Code: (int) 0,
     Output: (string) (len=2) "US",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .aaa \"var_a_from_task\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwith default value\nin block func\n",
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
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"{{.aaa}}\"",
        "echo \"{{.loopitem}}\""
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
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "China"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "China",
      "loopindex": 2
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"var_a_from_task\"",
     Code: (int) 0,
     Output: (string) (len=15) "var_a_from_task",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "China"
    -
    China
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"China\"",
     Code: (int) 0,
     Output: (string) (len=5) "China",
     ErrMsg: (string) ""
    }
    
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .aaa \"var_a_from_task\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwith default value\nin block func\n",
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
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"{{.aaa}}\"",
        "echo \"{{.loopitem}}\""
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
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"var_a_from_task\"",
     Code: (int) 0,
     Output: (string) (len=15) "var_a_from_task",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Japan"
    -
    Japan
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"Japan\"",
     Code: (int) 0,
     Output: (string) (len=5) "Japan",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0164 log - verbose level v](../../logs/c0164_v)
* [c0164 log - verbose level vv](../../logs/c0164_vv)
* [c0164 log - verbose level vvv](../../logs/c0164_vvv)
* [c0164 log - verbose level vvvv](../../logs/c0164_vvvv)
* [c0164 log - verbose level vvvvv](../../logs/c0164_vvvvv)

##### References
* [Related Chapter](../../block-func/c0164)
