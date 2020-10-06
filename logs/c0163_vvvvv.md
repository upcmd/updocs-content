---
title: "c0163_vvvvv"
date: 2020-10-06T23:46:22+1010:00
draft: false
weight: 11634

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0163
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
    loading [Task]:  ./tests/functests/c0163
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000967a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000c60f8)({
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
        "sub_task"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: {
        {
          Name: "aaa",
          Value: "var_a_from_task",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
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
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 0
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
              "name": "assert",
              "cmd": {
                "{{eq .aaa \"var_a_from_task\"}}"
              }
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
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
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
      "up_runtime_task_layer_number": 1
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
      "up_runtime_task_layer_number": 1
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
      "loopindex": 0,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopindex1": 1,
      "loopitem": "Austraila"
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
      "loopindex1": 1,
      "loopitem": "Austraila",
      "loopindex": 0
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
      "loopindex1": 1,
      "loopitem": "Austraila",
      "loopindex": 0
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
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US"
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US"
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US",
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US"
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US",
      "up_runtime_task_layer_number": 1
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "US",
      "up_runtime_task_layer_number": 1
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
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
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
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3
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
      "loopindex1": 3,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
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
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "Japan",
      "loopindex": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "Japan",
      "loopindex": 3
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
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
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
* [c0163 log - verbose level v](../../logs/c0163_v)
* [c0163 log - verbose level vv](../../logs/c0163_vv)
* [c0163 log - verbose level vvv](../../logs/c0163_vvv)
* [c0163 log - verbose level vvvv](../../logs/c0163_vvvv)
* [c0163 log - verbose level vvvvv](../../logs/c0163_vvvvv)

##### References
* [Related Chapter](../../block-func/c0163)
