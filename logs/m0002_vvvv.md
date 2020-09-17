---
title: "0002_vvvv"
date: 2020-09-18T00:52:27+99:00
draft: false
weight: 100203

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0002/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0002
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0002
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
    work dir: /up_project/up/tests/modtests/0002
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
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [dev], exec profile: []
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
      "a": "caller-aaa",
      "b": "module-bbb"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa",
      "b": "module-bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    ... module world
    a: caller-aaa
    b: module-bbb
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    
```

##### Logs with different verbose level
* [m0002 log - verbose level v](../../logs/m0002_v)
* [m0002 log - verbose level vv](../../logs/m0002_vv)
* [m0002 log - verbose level vvv](../../logs/m0002_vvv)
* [m0002 log - verbose level vvvv](../../logs/m0002_vvvv)
* [m0002 log - verbose level vvvvv](../../logs/m0002_vvvvv)

##### References
* [Related Chapter](../../module/0002)
