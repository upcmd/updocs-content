---
title: "c0108_vvvv"
date: 2020-07-01T15:34:35+77:00
draft: false
weight: 11083

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0108
                 Verbose -> vvvv
              ModuleName -> happy_newton7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0108
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [happy_newton7] instance id: [dev]
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
    
    happy_newton7: overall final exec vars:
    
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
          "desc": "jerry is in local scope so there is no value",
          "cmd": "{{.jerry}}"
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
    
    happy_newton7: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom"
    })
    
    ~SubStep1: [print: jerry is in local scope so there is no value ]
    <no value>
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the dvar value of jerry",
          "cmd": "{{.jerry}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "jerry",
          Value: "this is jerry in task scope",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskscope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
    
    happy_newton7: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskscope",
          "cmd": "{{.jerry}}"
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
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    happy_newton7: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    ~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskscope ]
    this is jerry in task scope
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "var jerry in task scope is overrided by local var jerry",
          "cmd": "{{.jerry}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "jerry is overrided in local scope"
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
      "jerry": "jerry is overrided in local scope"
    })
    
    happy_newton7: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "jerry is overrided in local scope"
    })
    
    ~SubStep1: [print: var jerry in task scope is overrided by local var jerry ]
    jerry is overrided in local scope
    -Step6:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the jerry defined in task var scope",
          "cmd": "{{.jerry}}"
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
      "jerry": "this is jerry in task scope"
    })
    
    happy_newton7: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    ~SubStep1: [print: this should print out the jerry defined in task var scope ]
    this is jerry in task scope
    
```

##### Logs with different verbose level
* [c0108 log - verbose level v](../../logs/c0108_v)
* [c0108 log - verbose level vv](../../logs/c0108_vv)
* [c0108 log - verbose level vvv](../../logs/c0108_vvv)
* [c0108 log - verbose level vvvv](../../logs/c0108_vvvv)
* [c0108 log - verbose level vvvvv](../../logs/c0108_vvvvv)

##### References
* [Related Chapter](../../vars/c0108)
