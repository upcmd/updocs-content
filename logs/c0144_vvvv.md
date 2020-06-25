---
title: "c0144_vvvv"
date: 2020-06-25T01:56:06+66:00
draft: false
weight: 11443

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0144
                 Verbose -> vvvv
              ModuleName -> kickass_poincare3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0144
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [kickass_poincare3] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: main job ]
    {
      Name: "",
      Do: {
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "main job",
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
    
    kickass_poincare3: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0144 log - verbose level v](../../logs/c0144_v)
* [c0144 log - verbose level vv](../../logs/c0144_vv)
* [c0144 log - verbose level vvv](../../logs/c0144_vvv)
* [c0144 log - verbose level vvvv](../../logs/c0144_vvvv)
* [c0144 log - verbose level vvvvv](../../logs/c0144_vvvvv)

##### References
* [Related Chapter](../../usage/c0144)
