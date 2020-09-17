---
title: "0001_vvvv"
date: 2020-09-18T01:28:26+99:00
draft: false
weight: 100103

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0001/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0001
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0001
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0001
    -exec task: Main
    loading [Task]:  ./up.yml
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
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: main job ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello world"
    
    cmd=>:
    echo "hello world"
    -
    hello world
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    this is a internal task
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "a": "aaa"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "a": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [print:  ]
    ... world
    
```

##### Logs with different verbose level
* [m0001 log - verbose level v](../../logs/m0001_v)
* [m0001 log - verbose level vv](../../logs/m0001_vv)
* [m0001 log - verbose level vvv](../../logs/m0001_vvv)
* [m0001 log - verbose level vvvv](../../logs/m0001_vvvv)
* [m0001 log - verbose level vvvvv](../../logs/m0001_vvvvv)

##### References
* [Related Chapter](../../module/0001)
