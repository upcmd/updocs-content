---
title: "c0094_vvvv"
date: 2020-06-27T03:09:27+66:00
draft: false
weight: 10943

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0094
                 Verbose -> vvvv
              ModuleName -> drunk_yalow7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0094
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [drunk_yalow7] instance id: [dev]
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
        "layer2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "layer1_bbb": "layer1_bbb",
        "layer1_aaa": "layer1_aaa"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "layer1-tom",
        "layer1-peter",
        "layer1-james"
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
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
          "cmd": "hello {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "hello layer1_aaa: {{.layer1_aaa}}"
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
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-tom
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "hello layer1_bbb: {{.layer1_bbb}}"
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
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-tom
    ~~SubStep2: [print:  ]
    hello layer1_bbb: layer1_bbb
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "hello layer1_aaa: {{.layer1_aaa}}"
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
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-peter
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "hello layer1_bbb: {{.layer1_bbb}}"
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
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-peter
    ~~SubStep2: [print:  ]
    hello layer1_bbb: layer1_bbb
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "hello {{.loopitem}}",
          "name": "print"
        },
        {
          "cmd": "hello layer1_aaa: {{.layer1_aaa}}",
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
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-james
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "hello layer1_bbb: {{.layer1_bbb}}"
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
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1,
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer1_aaa": "layer1_aaa"
    })
    
    drunk_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1,
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer1_aaa": "layer1_aaa"
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-james
    ~~SubStep2: [print:  ]
    hello layer1_bbb: layer1_bbb
    
```

##### Logs with different verbose level
* [c0094 log - verbose level v](../../logs/c0094_v)
* [c0094 log - verbose level vv](../../logs/c0094_vv)
* [c0094 log - verbose level vvv](../../logs/c0094_vvv)
* [c0094 log - verbose level vvvv](../../logs/c0094_vvvv)
* [c0094 log - verbose level vvvvv](../../logs/c0094_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0094)
