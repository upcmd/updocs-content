---
title: "c0091_vvvvv"
date: 2020-10-07T00:11:15+1010:00
draft: false
weight: 10914

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0091
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
    loading [Task]:  ./tests/functests/c0091
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e74a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc000096900)({
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa"
    })
    
    caller's vars to task (layer2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
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
        "layer3"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "layer2_aaa": "layer2_aaa",
        "layer2_bbb": "layer2_bbb"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "layer2-tom",
        "layer2-peter",
        "layer2-james"
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
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (layer3)::
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-peter"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-james
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer2)::
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
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
        "layer3"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "layer2_aaa": "layer2_aaa",
        "layer2_bbb": "layer2_bbb"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "layer2-tom",
        "layer2-peter",
        "layer2-james"
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
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "layer2_aaa": "layer2_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 2
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "layer2_aaa": "layer2_aaa"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.loopitem}}"
        },
        {
          "cmd": "hello layer1_aaa: {{.layer1_aaa}}",
          "name": "print"
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "layer2-james",
      "loopindex": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer2_bbb": "layer2_bbb",
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "layer2_aaa": "layer2_aaa"
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-james
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer2)::
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
    hello layer1_aaa: {{.layer1_aaa}}
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    {
      Name: "",
      Do: {
        "layer3"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "layer2_aaa": "layer2_aaa",
        "layer2_bbb": "layer2_bbb"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "layer2-tom",
        "layer2-peter",
        "layer2-james"
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
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2
    })
    
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "name": "print",
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa"
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    caller's vars to task (layer3)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
        },
        {
          "cmd": "hello layer2_aaa: {{.layer2_aaa}}",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2
    })
    
    hello {{.loopitem}}
    ~~~SubStep1: [print:  ]
    hello layer2-james
    hello layer1_aaa: {{.layer1_aaa}}
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    hello layer2_aaa: {{.layer2_aaa}}
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    
```

##### Logs with different verbose level
* [c0091 log - verbose level v](../../logs/c0091_v)
* [c0091 log - verbose level vv](../../logs/c0091_vv)
* [c0091 log - verbose level vvv](../../logs/c0091_vvv)
* [c0091 log - verbose level vvvv](../../logs/c0091_vvvv)
* [c0091 log - verbose level vvvvv](../../logs/c0091_vvvvv)

##### References
* [Related Chapter](../../loop/c0091)
