---
title: "c0160_vvvvv"
date: 2020-10-07T00:11:29+1010:00
draft: false
weight: 11604

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0160
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
    loading [Task]:  ./tests/functests/c0160
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000ca40)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e128)({
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
    
    -Step1: [
    test var overriding in sub_task
    ]
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
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    without default value
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
      Desc: "inspect if the correct parameter has been passed in correctly\nwithout default value\n",
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
        {
          "func": "cmd",
          "desc": "inspect if the correct parameter has been passed in correctly\nwithout default value\nin block func\n",
          "do": {
            {
              "name": "assert",
              "cmd": {
                "{{eq .aaa \"var_a_from_task\"}}"
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    without default value
    in block func
    ]
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "{{eq .aaa \"var_a_from_task\"}}"
          },
          "name": "assert"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwithout default value\nin block func\n",
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
    --Step3: [
    inspect if the correct parameter has been passed in correctly
    with default value
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
      Vars: {
        "aaa": "var_a_from_sub_task"
      },
      Dvars: <nil>,
      Desc: "inspect if the correct parameter has been passed in correctly\nwith default value\n",
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
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step4:
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
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    [{{eq .aaa "var_a_from_task"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    
```

##### Logs with different verbose level
* [c0160 log - verbose level v](../../logs/c0160_v)
* [c0160 log - verbose level vv](../../logs/c0160_vv)
* [c0160 log - verbose level vvv](../../logs/c0160_vvv)
* [c0160 log - verbose level vvvv](../../logs/c0160_vvvv)
* [c0160 log - verbose level vvvvv](../../logs/c0160_vvvvv)

##### References
* [Related Chapter](../../block-func/c0160)
