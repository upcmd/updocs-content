---
title: "c0105_vvvvv"
date: 2020-07-20T02:01:48+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0105
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001752a0)(<nil>)
    
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
          "name": "print",
          "cmd": "{{.tom}}"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
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
            "desc": "by default hitom is registered in to global context",
            "value": "hello, {{.tom}}",
            "name": "hitom"
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
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
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
      "hitom": "hello, this is tom",
      "tom": "this is tom"
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
          "cmd": "{{.hijerry}}",
          "name": "print",
          "desc": "expecting to see its value since it is still in same func scope"
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
      "hitom": "hello, this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
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
      "hitom": "hello, this is tom",
      "hijerry": "hello, jerry"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
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
