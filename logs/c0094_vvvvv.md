---
title: "c0094_vvvvv"
date: 2020-07-20T02:01:45+77:00
draft: false
weight: 10944

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0094
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000cb40)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
      Vars: {
        "layer1_aaa": "layer1_aaa",
        "layer1_bbb": "layer1_bbb"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    caller's vars to task (layer2)::
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
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
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-tom
    hello layer1_aaa: {{.layer1_aaa}}
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
          "cmd": "hello layer1_bbb: {{.layer1_bbb}}",
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
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer1_aaa": "layer1_aaa",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer1_aaa": "layer1_aaa",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "layer1_aaa": "layer1_aaa",
      "up_runtime_task_layer_number": 1,
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-tom
    hello layer1_bbb: {{.layer1_bbb}}
    ~~SubStep2: [print:  ]
    hello layer1_bbb: layer1_bbb
    caller's vars to task (layer2)::
    (*core.Cache)({
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1
    })
    
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
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "up_runtime_task_layer_number": 1,
      "layer1_bbb": "layer1_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "up_runtime_task_layer_number": 1,
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-peter
    hello layer1_aaa: {{.layer1_aaa}}
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
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1,
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 1
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-peter
    hello layer1_bbb: {{.layer1_bbb}}
    ~~SubStep2: [print:  ]
    hello layer1_bbb: layer1_bbb
    caller's vars to task (layer2)::
    (*core.Cache)({
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
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
          "cmd": "hello {{.loopitem}}",
          "name": "print"
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
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-james
    hello layer1_aaa: {{.layer1_aaa}}
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
          "cmd": "hello layer1_bbb: {{.layer1_bbb}}",
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
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james"
    })
    
    hello {{.loopitem}}
    ~~SubStep1: [print:  ]
    hello layer1-james
    hello layer1_bbb: {{.layer1_bbb}}
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
