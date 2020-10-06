---
title: "c0063_vvvv"
date: 2020-10-07T00:11:10+1010:00
draft: false
weight: 10633

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0063
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
    loading [Task]:  ./tests/functests/c0063
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
      "a": "global-var-a"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "global-var-a"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "global-var-a",
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "runtime-var-b",
      "a": "global-var-a",
      "up_runtime_task_layer_number": 0
    })
    
    Enter Value For [pause action to continue]: 
    
    enter: continue 
        q: quit
        i: inspect
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"
    -
    hello
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.a}}"
    
    cmd=>:
    echo "hello global-var-a"
    -
    hello global-var-a
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "runtime-var-b",
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    Enter Value For [pause action to continue]: 
    
    enter: continue 
        q: quit
        i: inspect
    
    ~SubStep1: [print:  ]
    hello global-var-a
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "a": "global-var-a"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "next step"
    
    cmd=>:
    echo "next step"
    -
    next step
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0063 log - verbose level v](../../logs/c0063_v)
* [c0063 log - verbose level vv](../../logs/c0063_vv)
* [c0063 log - verbose level vvv](../../logs/c0063_vvv)
* [c0063 log - verbose level vvvv](../../logs/c0063_vvvv)
* [c0063 log - verbose level vvvvv](../../logs/c0063_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0063)
