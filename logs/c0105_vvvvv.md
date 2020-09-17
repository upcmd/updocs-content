---
title: "c0105_vvvvv"
date: 2020-09-18T01:27:38+99:00
draft: false
weight: 11054

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0105
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
    loading [Task]:  ./tests/functests/c0105
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef300)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      Do: {
        {
          "cmd": "{{.tom}}",
          "name": "print"
        },
        {
          "name": "print",
          "cmd": "{{.jerry}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "this is jerry"
      },
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    })
    
    {{.tom}}
    ~SubStep1: [print:  ]
    this is tom
    {{.jerry}}
    ~SubStep2: [print:  ]
    this is jerry
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "reg",
          "cmd": {
            "name": "hitom",
            "desc": "by default hitom is registered in to global context",
            "value": "hello, {{.tom}}"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    {{.jerry}}
    ~SubStep1: [print:  ]
    None
    map[desc:by default hitom is registered in to global context name:hitom value:hello, {{.tom}}]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "hitom": "hello, this is tom"
    })
    
    {{.hitom}}
    ~SubStep3: [print:  ]
    hello, this is tom
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "by default hitom is accessible from global context, that's why it is accessiable cross func",
          "cmd": "{{.hitom}}"
        },
        {
          "name": "reg",
          "cmd": {
            "name": "hijerry",
            "desc": "hijerry is registered to local scope only",
            "value": "hello, jerry"
          },
          "flags": {
            "localOnly"
          }
        },
        {
          "name": "print",
          "desc": "expecting to see its value since it is still in same func scope",
          "cmd": "{{.hijerry}}"
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
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "hitom": "hello, this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "hitom": "hello, this is tom",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "hitom": "hello, this is tom",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    {{.hitom}}
    ~SubStep1: [print: by default hitom is accessible from global context, that's why it is accessiable cross func ]
    hello, this is tom
    map[desc:hijerry is registered to local scope only name:hijerry value:hello, jerry]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "hijerry": "hello, jerry",
      "hitom": "hello, this is tom"
    })
    
    {{.hijerry}}
    ~SubStep3: [print: expecting to see its value since it is still in same func scope ]
    hello, jerry
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "hijerry is not accessible here and got <no value>",
          "cmd": "{{.hijerry}}"
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
      "tom": "this is tom",
      "hitom": "hello, this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "hitom": "hello, this is tom",
      "up_runtime_task_layer_number": 0,
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "hitom": "hello, this is tom",
      "up_runtime_task_layer_number": 0,
      "tom": "this is tom"
    })
    
    {{.hijerry}}
    ~SubStep1: [print: hijerry is not accessible here and got <no value> ]
    None
    
```

##### Logs with different verbose level
* [c0105 log - verbose level v](../../logs/c0105_v)
* [c0105 log - verbose level vv](../../logs/c0105_vv)
* [c0105 log - verbose level vvv](../../logs/c0105_vvv)
* [c0105 log - verbose level vvvv](../../logs/c0105_vvvv)
* [c0105 log - verbose level vvvvv](../../logs/c0105_vvvvv)

##### References
* [Related Chapter](../../vars/c0105)
