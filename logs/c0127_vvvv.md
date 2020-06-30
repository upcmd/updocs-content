---
title: "c0127_vvvv"
date: 2020-07-01T15:34:39+77:00
draft: false
weight: 11273

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0127
                 Verbose -> vvvv
              ModuleName -> pensive_yalow4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0127
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [pensive_yalow4] instance id: [dev]
    merged[ dev ] runtime vars:
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
        {
          "cmd": "true/false value of goahead:\n{{.goahead}}\n{{not .goahead}}\n",
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
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    <no value>
    true
    
    -Step2: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    {
      Name: "",
      Do: {
        "goahead"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "show example the route goes to call goelse for the condition of not if condition succeeds",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: "goelse",
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    condition failed, skip executing step 
    
    -Step3: [: show example the else coud route to call a list of tasks ]
    {
      Name: "",
      Do: {
        "goahead"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "show example the else coud route to call a list of tasks",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: {
        "goelse",
        "goelse",
        "goelse2",
        "goelse2"
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    condition failed, skip executing step 
    
    -Step4: [: show it is same that you could assemble a list of tasks for if true condition ]
    {
      Name: "",
      Do: {
        "goahead",
        "goahead",
        "goahead"
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
      If: "{{.goahead}}",
      Else: {
        "goelse",
        "goelse",
        "goelse2",
        "goelse2"
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
      "goahead": true
    })
    
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "go ahead .......",
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
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "go ahead .......",
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
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "go ahead ......."
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
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    pensive_yalow4: overall final exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
    
```

##### Logs with different verbose level
* [c0127 log - verbose level v](../../logs/c0127_v)
* [c0127 log - verbose level vv](../../logs/c0127_vv)
* [c0127 log - verbose level vvv](../../logs/c0127_vvv)
* [c0127 log - verbose level vvvv](../../logs/c0127_vvvv)
* [c0127 log - verbose level vvvvv](../../logs/c0127_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0127)
