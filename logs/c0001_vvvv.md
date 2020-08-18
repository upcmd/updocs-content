---
title: "c0001_vvvv"
date: 2020-08-18T15:15:47+88:00
draft: false
weight: 10013

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0001
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0001
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: say hello world in shell ]
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
    
    cmd=>:
    echo "hello"
    -
    hello
    -
     .. ok
    cmd( 2):
    echo "world"
    
    cmd=>:
    echo "world"
    -
    world
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0001 log - verbose level v](../../logs/c0001_v)
* [c0001 log - verbose level vv](../../logs/c0001_vv)
* [c0001 log - verbose level vvv](../../logs/c0001_vvv)
* [c0001 log - verbose level vvvv](../../logs/c0001_vvvv)
* [c0001 log - verbose level vvvvv](../../logs/c0001_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0001)
