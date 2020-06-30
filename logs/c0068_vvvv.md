---
title: "c0068_vvvv"
date: 2020-07-01T15:34:30+77:00
draft: false
weight: 10683

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0068
                 Verbose -> vvvv
              ModuleName -> condescending_shockley7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0068
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [condescending_shockley7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"world\"|grep non-exist",
        "echo \"world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do step1 in shell func",
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
    
    condescending_shockley7: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    cmd( 2):
    echo "world"|grep non-exist
    
     \_ echo "world"|grep non-exist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    cmd( 3):
    echo "world"
    
     \_ echo "world"
    world
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0068 log - verbose level v](../../logs/c0068_v)
* [c0068 log - verbose level vv](../../logs/c0068_vv)
* [c0068 log - verbose level vvv](../../logs/c0068_vvv)
* [c0068 log - verbose level vvvv](../../logs/c0068_vvvv)
* [c0068 log - verbose level vvvvv](../../logs/c0068_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0068)
