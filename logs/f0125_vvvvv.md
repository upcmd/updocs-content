---
title: "f0125_vvvvv"
date: 2020-06-25T01:56:09+66:00
draft: false
weight: 11254

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0125
                 Verbose -> vvvvv
              ModuleName -> condescending_ritchie0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/f0125
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed2a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [condescending_ritchie0] instance id: [dev]
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
        "layer2"
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
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (layer2)::
    (*core.Cache)({
    })
    
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}"
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    ~~SubStep1: [print:  ]
    up_runtime_task_layer_number: 1
    --Step2:
    {
      Name: "",
      Do: {
        "layer3"
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
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (layer3)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "name": "exit"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq  .up_runtime_task_layer_number 4}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    condition failed, skip executing step 
    
    ---Step2:
    {
      Name: "",
      Do: {
        "layer2"
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
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    caller's vars to task (layer2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
      located task-> 2 [layer2]: 
    ===Task2: [task/layer2/layer3 ==> layer2:  ]
    Executing task stack layer: 4
    
    ----Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}"
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
      "up_runtime_task_layer_number": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 3
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    ~~~~SubStep1: [print:  ]
    up_runtime_task_layer_number: 3
    ----Step2:
    {
      Name: "",
      Do: {
        "layer3"
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
      "up_runtime_task_layer_number": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 3
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
    caller's vars to task (layer3)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
      located task-> 3 [layer3]: 
    ====Task3: [task/layer2/layer3/layer2 ==> layer3:  ]
    Executing task stack layer: 5
    
    -----Step1:
    {
      Name: "",
      Do: {
        {
          "name": "exit"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq  .up_runtime_task_layer_number 4}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 4
    }
    
    
    condescending_ritchie0: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 4
    })
    
    ~~~~~SubStep1: [exit:  ]
      Exit: exit [client choose to exit]
    
```

##### Logs with different verbose level
* [f0125 log - verbose level v](../../logs/f0125_v)
* [f0125 log - verbose level vv](../../logs/f0125_vv)
* [f0125 log - verbose level vvv](../../logs/f0125_vvv)
* [f0125 log - verbose level vvvv](../../logs/f0125_vvvv)
* [f0125 log - verbose level vvvvv](../../logs/f0125_vvvvv)

##### References
* [Related Chapter](../../loop/f0125)