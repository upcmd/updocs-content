---
title: "c0002_vvvv"
date: 2020-10-06T23:45:50+1010:00
draft: false
weight: 10023

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0002
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0002
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: this is task ]
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
    -Step2: [: do step2 in shell func ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
    echo "I got exception"|grep non-exist
    
    cmd=>:
    echo "I got exception"|grep non-exist
    -
    
    -
     .. failed(suppressed if it is not the last step)
    cmd( 3):
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
* [c0002 log - verbose level v](../../logs/c0002_v)
* [c0002 log - verbose level vv](../../logs/c0002_vv)
* [c0002 log - verbose level vvv](../../logs/c0002_vvv)
* [c0002 log - verbose level vvvv](../../logs/c0002_vvvv)
* [c0002 log - verbose level vvvvv](../../logs/c0002_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0002)
