---
title: "c0127_vvvvv"
date: 2020-09-18T01:27:43+99:00
draft: false
weight: 11274

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
    loading [Task]:  ./tests/functests/c0127
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001776e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "goahead": false
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "goahead": (bool) false
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "goahead": false
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "true/false value of goahead:\n{{.goahead}}\n{{not .goahead}}\n"
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
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "goahead": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    true/false value of goahead:
    {{.goahead}}
    {{not .goahead}}
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    else caller vars to task (goelse)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else .......
    ~~SubStep1: [print:  ]
    do something else .......
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    else caller vars to task (goelse)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else ......."
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
      "up_runtime_task_layer_number": 1,
      "goahead": false
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else .......
    ~~SubStep1: [print:  ]
    do something else .......
    else caller vars to task (goelse)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else .......
    ~~SubStep1: [print:  ]
    do something else .......
    else caller vars to task (goelse2)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 4 [goelse2]: 
    =Task4: [task ==> goelse2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else2 ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else2 .......
    ~~SubStep1: [print:  ]
    do something else2 .......
    else caller vars to task (goelse2)::
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 4 [goelse2]: 
    =Task4: [task ==> goelse2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "do something else2 ......."
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
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": false,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    do something else2 .......
    ~~SubStep1: [print:  ]
    do something else2 .......
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": true,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (goahead)::
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": true,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    go ahead .......
    ~~SubStep1: [print:  ]
    go ahead .......
    caller's vars to task (goahead)::
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "goahead": true
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    go ahead .......
    ~~SubStep1: [print:  ]
    go ahead .......
    caller's vars to task (goahead)::
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "goahead": true,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    go ahead .......
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
