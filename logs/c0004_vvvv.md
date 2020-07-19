---
title: "c0004_vvvv"
date: 2020-07-20T02:01:29+77:00
draft: false
weight: 10043

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0004
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0004
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
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: this is task1 ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    echo "world"
    
    
    cmd=>:
    echo "hello"
    echo "world"
    <=
    hello
    world
     .. ok
    cmd( 2):
    echo "how are you"
    
    cmd=>:
    echo "how are you"<=
    how are you
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0004 log - verbose level v](../../logs/c0004_v)
* [c0004 log - verbose level vv](../../logs/c0004_vv)
* [c0004 log - verbose level vvv](../../logs/c0004_vvv)
* [c0004 log - verbose level vvvv](../../logs/c0004_vvvv)
* [c0004 log - verbose level vvvvv](../../logs/c0004_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0004)
