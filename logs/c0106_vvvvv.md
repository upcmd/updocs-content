---
title: "c0106_vvvvv"
date: 2020-07-01T15:34:35+77:00
draft: false
weight: 11064

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0106
                 Verbose -> vvvvv
              ModuleName -> backstabbing_lumiere4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0106
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed560)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [backstabbing_lumiere4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom"
    }
    
    (core.Cache) (len=1) {
     (string) (len=3) "tom": (string) (len=11) "this is tom"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "sub1",
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
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom"
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    caller's vars to task (sub1)::
    (*core.Cache)({
      "tom": "this is tom"
    })
    
      located task-> 2 [sub1]: 
    =Task2: [task ==> sub1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "name": "hitom",
            "desc": "by default hitom is registered in to global context",
            "value": "hello, {{.tom}}"
          },
          "flags": {
            "localonly"
          }
        },
        {
          "name": "print",
          "cmd": "{{.hitom}}"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    map[desc:by default hitom is registered in to global context name:hitom value:hello, {{.tom}}]
    ~~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom"
    })
    
    {{.hitom}}
    ~~SubStep2: [print:  ]
    hello, this is tom
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "should be <no value> since it is marked localonly",
          "cmd": "{{.hitom}}"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    {{.hitom}}
    ~~SubStep1: [print: should be <no value> since it is marked localonly ]
    <no value>
    -Step2: [: check if hitom is available in global context
    it should be <no value> as hitom in sub1 is marked localonly
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.hitom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "check if hitom is available in global context\nit should be <no value> as hitom in sub1 is marked localonly\n",
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom"
    })
    
    {{.hitom}}
    ~SubStep1: [print:  ]
    <no value>
    -Step3:
    {
      Name: "",
      Do: "sub2",
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (sub2)::
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [sub2]: 
    =Task3: [task ==> sub2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "name": "hitom",
            "desc": "by default hitom is registered in to global context",
            "value": "hello, {{.tom}}"
          }
        },
        {
          "cmd": "{{.hitom}}",
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    map[desc:by default hitom is registered in to global context name:hitom value:hello, {{.tom}}]
    ~~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "hitom": "hello, this is tom",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom"
    })
    
    {{.hitom}}
    ~~SubStep2: [print:  ]
    hello, this is tom
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "by default hitom is accessible from global context, that's why it is accessiable cross func\nhowever this is only available in its own call stack global but not return and available to its parent var scope\n",
          "cmd": "{{.hitom}}"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom",
      "tom": "this is tom"
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "hitom": "hello, this is tom"
    })
    
    {{.hitom}}
    ~~SubStep1: [print: by default hitom is accessible from global context, that's why it is accessiable cross func
    however this is only available in its own call stack global but not return and available to its parent var scope
     ]
    hello, this is tom
    -Step4: [: check if hitom is available in global context
    though hitom was regiser as global var, but it was registered to its own call stack
    however this is only available in its own call stack global but not return and available to its parent var scope
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.hitom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "check if hitom is available in global context\nthough hitom was regiser as global var, but it was registered to its own call stack\nhowever this is only available in its own call stack global but not return and available to its parent var scope\n",
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    backstabbing_lumiere4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    {{.hitom}}
    ~SubStep1: [print:  ]
    <no value>
    
```

##### Logs with different verbose level
* [c0106 log - verbose level v](../../logs/c0106_v)
* [c0106 log - verbose level vv](../../logs/c0106_vv)
* [c0106 log - verbose level vvv](../../logs/c0106_vvv)
* [c0106 log - verbose level vvvv](../../logs/c0106_vvvv)
* [c0106 log - verbose level vvvvv](../../logs/c0106_vvvvv)

##### References
* [Related Chapter](../../vars/c0106)
