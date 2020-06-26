---
title: "c0110_vvvvv"
date: 2020-06-27T03:09:29+66:00
draft: false
weight: 11104

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0110
                 Verbose -> vvvvv
              ModuleName -> high_ardinghelli3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0110
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001853e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [high_ardinghelli3] instance id: [dev]
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
        "subtask1"
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
      Loop: {
        "tom",
        "jerry",
        "emily"
      },
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
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopindex1}}:{{.loopitem}}"
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    {{.loopindex1}}:{{.loopitem}}
    ~~SubStep1: [print:  ]
    1:tom
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .loopitem \"tom\"}}"
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
      If: "{{eq .loopindex1 1}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [{{eq .loopitem "tom"}}]
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .loopitem "tom"}}]
    --Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.person}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": "{{.loopitem}}"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopitem": "tom",
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopitem": "tom"
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "loopitem": "tom",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    {{.person}}
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.theone}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "theone",
          Value: "{{.loopitem}}",
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
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
      "theone": "tom"
    }
    
    
    scope[local] merged: {
      "theone": "tom",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "tom",
      "loopindex": 0,
      "theone": "tom"
    })
    
    {{.theone}}
    ~~SubStep1: [print:  ]
    tom
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.loopindex1}}:{{.loopitem}}",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1,
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1
    })
    
    {{.loopindex1}}:{{.loopitem}}
    ~~SubStep1: [print:  ]
    2:jerry
    --Step2:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "{{eq .loopitem \"tom\"}}"
          },
          "name": "assert"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .loopindex1 1}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "up_runtime_task_layer_number": 1
    })
    
    condition failed, skip executing step 
    
    --Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.person}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": "{{.loopitem}}"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "person": "{{.loopitem}}",
      "up_runtime_task_layer_number": 1,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "person": "{{.loopitem}}"
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "jerry",
      "person": "{{.loopitem}}"
    })
    
    {{.person}}
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.theone}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "theone",
          Value: "{{.loopitem}}",
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
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
      "theone": "jerry"
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "theone": "jerry",
      "loopitem": "jerry"
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "jerry",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "theone": "jerry"
    })
    
    {{.theone}}
    ~~SubStep1: [print:  ]
    jerry
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopindex1}}:{{.loopitem}}"
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
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily"
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    {{.loopindex1}}:{{.loopitem}}
    ~~SubStep1: [print:  ]
    3:emily
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "assert",
          "cmd": {
            "{{eq .loopitem \"tom\"}}"
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
      If: "{{eq .loopindex1 1}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily",
      "loopindex": 2
    })
    
    condition failed, skip executing step 
    
    --Step3:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.person}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": "{{.loopitem}}"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopindex": 2
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "loopitem": "emily",
      "up_runtime_task_layer_number": 1,
      "person": "{{.loopitem}}",
      "loopindex": 2
    })
    
    {{.person}}
    ~~SubStep1: [print:  ]
    {{.loopitem}}
    --Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.theone}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "theone",
          Value: "{{.loopitem}}",
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
      "loopitem": "emily",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
      "theone": "emily"
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily",
      "theone": "emily"
    }
    
    
    high_ardinghelli3: overall final exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "emily",
      "theone": "emily"
    })
    
    {{.theone}}
    ~~SubStep1: [print:  ]
    emily
    
```

##### Logs with different verbose level
* [c0110 log - verbose level v](../../logs/c0110_v)
* [c0110 log - verbose level vv](../../logs/c0110_vv)
* [c0110 log - verbose level vvv](../../logs/c0110_vvv)
* [c0110 log - verbose level vvvv](../../logs/c0110_vvvv)
* [c0110 log - verbose level vvvvv](../../logs/c0110_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0110)
