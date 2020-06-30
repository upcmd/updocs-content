---
title: "c0140_vvvv"
date: 2020-07-01T15:34:41+77:00
draft: false
weight: 11403

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0140
                 Verbose -> vvvv
              ModuleName -> angry_leakey5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0140
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [angry_leakey5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "I am the main entry"
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
    
    angry_leakey5: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    I am the main entry
    
```

##### Logs with different verbose level
* [c0140 log - verbose level v](../../logs/c0140_v)
* [c0140 log - verbose level vv](../../logs/c0140_vv)
* [c0140 log - verbose level vvv](../../logs/c0140_vvv)
* [c0140 log - verbose level vvvv](../../logs/c0140_vvvv)
* [c0140 log - verbose level vvvvv](../../logs/c0140_vvvvv)

##### References
* [Related Chapter](../../usage/c0140)
