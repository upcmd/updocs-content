---
title: "c0161_vvvvv"
date: 2020-09-18T00:51:52+99:00
draft: false
weight: 11614

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0161
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
    loading [Task]:  ./tests/functests/c0161
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf3c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    
    -Step1: [: test var overriding in sub_task
     ]
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
        }
      },
      Desc: "test var overriding in sub_task\n",
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
      "aaa": "var_a_from_task"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step2:
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
      "aaa": "var_a_from_task"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
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
            "echo \"{{.aaa}}\""
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    --Step1: [: inspect if the correct parameter has been passed in correctly
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
      "aaa": "var_a_from_task"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"{{.aaa}}\""
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
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
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
    
    . ok
    
```

##### Logs with different verbose level
* [c0161 log - verbose level v](../../logs/c0161_v)
* [c0161 log - verbose level vv](../../logs/c0161_vv)
* [c0161 log - verbose level vvv](../../logs/c0161_vvv)
* [c0161 log - verbose level vvvv](../../logs/c0161_vvvv)
* [c0161 log - verbose level vvvvv](../../logs/c0161_vvvvv)

##### References
* [Related Chapter](../../block-func/c0161)
