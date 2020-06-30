---
title: "c0139_vvvv"
date: 2020-07-01T15:34:41+77:00
draft: false
weight: 11393

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0139
                 Verbose -> vvvv
              ModuleName -> evil_turing8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0139
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [evil_turing8] instance id: [dev]
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
          "cmd": "step1"
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
    
    evil_turing8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    step1
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "fail"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": "tom"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .person \"tom-s-name\"}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "person": "tom"
    })
    
    evil_turing8: overall final exec vars:
    
    (*core.Cache)({
      "person": "tom"
    })
    
    condition failed, skip executing step 
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "cmdy": "step2",
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
    })
    
    evil_turing8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
     WARN: [cmd] - [lacking detailed implementation yet]
    
```

##### Logs with different verbose level
* [c0139 log - verbose level v](../../logs/c0139_v)
* [c0139 log - verbose level vv](../../logs/c0139_vv)
* [c0139 log - verbose level vvv](../../logs/c0139_vvv)
* [c0139 log - verbose level vvvv](../../logs/c0139_vvvv)
* [c0139 log - verbose level vvvvv](../../logs/c0139_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0139)
