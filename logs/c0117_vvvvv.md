---
title: "c0117_vvvvv"
date: 2020-10-06T23:46:12+1010:00
draft: false
weight: 11174

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0117
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
    loading [Task]:  ./tests/functests/c0117
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed460)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc000130910)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [step2: call subtask and exam the return value in following steps ]
    {
      Name: "step2",
      Do: "subtask",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "call subtask and exam the return value in following steps",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "proc 1",
        "proc 2",
        "proc 3"
      },
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
    
    caller's vars to task (subtask)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 1
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    {
      Name: "step2",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is the local defined loopitem",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item2
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    {
      Name: "step3",
      Do: {
        {
          "name": "print",
          "cmd": "parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "parentLoopItem",
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
      Desc: "demo use both loopitem in same context\nthe dvar parentLoopItem will map the value of parent loopitem\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
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
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
      "parentLoopItem": "proc 1"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "parentLoopItem": "proc 1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "parentLoopItem": "proc 1",
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1"
    })
    
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item1
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item2
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item3
    caller's vars to task (subtask)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 2
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    {
      Name: "step2",
      Do: {
        {
          "cmd": "{{.loopitem}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is the local defined loopitem",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
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
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item2
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    {
      Name: "step3",
      Do: {
        {
          "name": "print",
          "cmd": "parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "parentLoopItem",
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
      Desc: "demo use both loopitem in same context\nthe dvar parentLoopItem will map the value of parent loopitem\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
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
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
      "parentLoopItem": "proc 2"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "parentLoopItem": "proc 2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "parentLoopItem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item1
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item2
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item3
    caller's vars to task (subtask)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 3
    --Step2: [step2: the loopitem here is the local defined loopitem ]
    {
      Name: "step2",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is the local defined loopitem",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item2
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item3
    --Step3: [
    step3demo use both loopitem in same context
    the dvar parentLoopItem will map the value of parent loopitem
    ]
    {
      Name: "step3",
      Do: {
        {
          "name": "print",
          "cmd": "parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "parentLoopItem",
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
      Desc: "demo use both loopitem in same context\nthe dvar parentLoopItem will map the value of parent loopitem\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3"
      },
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
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
      "parentLoopItem": "proc 3"
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "parentLoopItem": "proc 3"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "parentLoopItem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item1
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item2
    parent loop: {{.parentLoopItem}}, child loop: {{.loopitem}}
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item3
    
```

##### Logs with different verbose level
* [c0117 log - verbose level v](../../logs/c0117_v)
* [c0117 log - verbose level vv](../../logs/c0117_vv)
* [c0117 log - verbose level vvv](../../logs/c0117_vvv)
* [c0117 log - verbose level vvvv](../../logs/c0117_vvvv)
* [c0117 log - verbose level vvvvv](../../logs/c0117_vvvvv)

##### References
* [Related Chapter](../../loop/c0117)
