---
title: "c0138_vvvv"
date: 2020-06-27T03:09:33+66:00
draft: false
weight: 11383

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0138
                 Verbose -> vvvv
              ModuleName -> kickass_almeida9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0138
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [kickass_almeida9] instance id: [dev]
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
        {
          "name": "print",
          "cmdy": "step1"
        },
        {
          "name": "print",
          "cmdx": "step2"
        },
        {
          "name": "print",
          "cmd": "step3"
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
    })
    
    kickass_almeida9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    ~SubStep2: [print:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep3: [print:  ]
    step3
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmdy": "step4"
        },
        {
          "namex": "exit"
        },
        {
          "namex": "break"
        },
        {
          "name": "print",
          "cmdy": "step4"
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
    })
    
    kickass_almeida9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    ~SubStep2: [:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep3: [:  ]
     WARN: [cmd] - [temporarily deactivated]
    ~SubStep4: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "step5"
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
    })
    
    kickass_almeida9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    step5
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmdx": "step6"
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
    })
    
    kickass_almeida9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [temporarily deactivated]
    
```

##### Logs with different verbose level
* [c0138 log - verbose level v](../../logs/c0138_v)
* [c0138 log - verbose level vv](../../logs/c0138_vv)
* [c0138 log - verbose level vvv](../../logs/c0138_vvv)
* [c0138 log - verbose level vvvv](../../logs/c0138_vvvv)
* [c0138 log - verbose level vvvvv](../../logs/c0138_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0138)
