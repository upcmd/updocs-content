---
title: "c0107_vvvvv"
date: 2020-06-25T01:55:58+66:00
draft: false
weight: 11074

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0107
                 Verbose -> vvvvv
              ModuleName -> happy_bell4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0107
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed320)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [happy_bell4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    }
    
    (core.Cache) (len=2) {
     (string) (len=3) "tom": (string) (len=21) "this is tom in global",
     (string) (len=5) "jerry": (string) (len=23) "this is jerry in global"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "sub",
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
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    caller's vars to task (sub)::
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
      located task-> 2 [sub]: 
    =Task2: [task ==> sub:  ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom 1 ]
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "desc": "by default tom is registered in to global context",
            "value": "tom created in sub",
            "name": "tom"
          },
          "name": "reg"
        },
        {
          "name": "print",
          "cmd": "in sub print1: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub func1"
      },
      Dvars: <nil>,
      Desc: "check value of tom 1",
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
      "john": "john in sub func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "john": "john in sub func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "john": "john in sub func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    map[desc:by default tom is registered in to global context name:tom value:tom created in sub]
    ~~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in sub"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub func1"
    })
    
    in sub print1: {{.tom}}
    ~~SubStep2: [print:  ]
    in sub print1: tom created in sub
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "trace",
          "cmd": "debug tom's value==>"
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
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    debug tom's value==>
    ~~SubStep1: [trace:  ]
    Trace:debug tom's value==>
    --Step3: [: check value of tom 2 ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in sub print2: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub func2"
      },
      Dvars: <nil>,
      Desc: "check value of tom 2",
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
      "john": "john in sub func2",
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "john": "john in sub func2",
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "john": "john in sub func2",
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    in sub print2: {{.tom}}
    ~~SubStep1: [print:  ]
    in sub print2: tom created in sub
    --Step4:
    {
      Name: "",
      Do: {
        {
          "name": "trace",
          "cmd": "<==debug tom's value"
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
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "tom created in sub",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    <==debug tom's value
    ~~SubStep1: [trace:  ]
    Trace:<==debug tom's value
    -Step2: [: check value of tom ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in main task print3: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "check value of tom",
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
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom in global"
    }
    
    
    happy_bell4: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom in global"
    })
    
    in main task print3: {{.tom}}
    ~SubStep1: [print:  ]
    in main task print3: this is tom in global
    
```

##### Logs with different verbose level
* [c0107 log - verbose level v](../../logs/c0107_v)
* [c0107 log - verbose level vv](../../logs/c0107_vv)
* [c0107 log - verbose level vvv](../../logs/c0107_vvv)
* [c0107 log - verbose level vvvv](../../logs/c0107_vvvv)
* [c0107 log - verbose level vvvvv](../../logs/c0107_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0107)