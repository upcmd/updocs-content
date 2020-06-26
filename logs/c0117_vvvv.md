---
title: "c0117_vvvv"
date: 2020-06-27T03:09:30+66:00
draft: false
weight: 11173

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
                 Verbose -> vvvv
              ModuleName -> silly_hoover2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0117
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [silly_hoover2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    })
    
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [step3: demo use both loopitem in same context
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "parentLoopItem": "proc 1"
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item2
    ~~SubStep1: [print:  ]
    parent loop: proc 1, child loop: item3
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    ~~SubStep1: [print:  ]
    proc 2
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [step3: demo use both loopitem in same context
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "parentLoopItem": "proc 2",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item2
    ~~SubStep1: [print:  ]
    parent loop: proc 2, child loop: item3
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    proc 3
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep1: [print:  ]
    item3
    --Step3: [step3: demo use both loopitem in same context
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "loopitem": "proc 3",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1
    })
    
    silly_hoover2: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "loopitem": "proc 3",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1,
      "parentLoopItem": "proc 3"
    })
    
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item1
    ~~SubStep1: [print:  ]
    parent loop: proc 3, child loop: item2
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
