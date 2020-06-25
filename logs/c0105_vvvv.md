---
title: "c0105_vvvv"
date: 2020-06-25T01:55:57+66:00
draft: false
weight: 11053

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
                 Verbose -> vvvv
              ModuleName -> modest_brattain2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0105
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [modest_brattain2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom"
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
    
    modest_brattain2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry"
    })
    
    ~SubStep1: [print:  ]
    this is tom
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    modest_brattain2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    ~SubStep1: [print:  ]
    <no value>
    ~SubStep2: [reg:  ]
    ~SubStep3: [print:  ]
    hello, this is tom
    -Step3:
    {
      Name: "",
      Do: {
        {
          "desc": "by default hitom is accessible from global context, that's why it is accessiable cross func",
          "cmd": "{{.hitom}}",
          "name": "print"
        },
        {
          "name": "reg",
          "cmd": {
            "value": "hello, jerry",
            "name": "hijerry",
            "desc": "hijerry is registered to local scope only"
          },
          "flags": {
            "localonly"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    modest_brattain2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    ~SubStep1: [print: by default hitom is accessible from global context, that's why it is accessiable cross func ]
    hello, this is tom
    ~SubStep2: [reg:  ]
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
    
    modest_brattain2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "hitom": "hello, this is tom"
    })
    
    ~SubStep1: [print: hijerry is not accessible here and got <no value> ]
    <no value>
    
```

##### Logs with different verbose level
* [c0105 log - verbose level v](../../logs/c0105_v)
* [c0105 log - verbose level vv](../../logs/c0105_vv)
* [c0105 log - verbose level vvv](../../logs/c0105_vvv)
* [c0105 log - verbose level vvvv](../../logs/c0105_vvvv)
* [c0105 log - verbose level vvvvv](../../logs/c0105_vvvvv)

##### References
* [Related Chapter](../../vars/c0105)