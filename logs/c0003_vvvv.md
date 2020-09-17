---
title: "c0003_vvvv"
date: 2020-09-18T01:27:20+99:00
draft: false
weight: 10033

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0003
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0003
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
    Task1: [task ==> task: this is task1 ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello"
    echo "world"
    
    
    cmd=>:
    echo "hello"
    echo "world"
    
    -
    hello
    world
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0003 log - verbose level v](../../logs/c0003_v)
* [c0003 log - verbose level vv](../../logs/c0003_vv)
* [c0003 log - verbose level vvv](../../logs/c0003_vvv)
* [c0003 log - verbose level vvvv](../../logs/c0003_vvvv)
* [c0003 log - verbose level vvvvv](../../logs/c0003_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0003)
