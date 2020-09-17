---
title: "c0087_vvvv"
date: 2020-09-18T00:51:35+99:00
draft: false
weight: 10873

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0087
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
    loading [Task]:  ./tests/functests/c0087
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
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo 'hello'
    
    cmd=>:
    echo 'hello'
    -
    hello
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [sleep:  ]
    sleeping 2000 milli seconds
    ....................
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    world
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [impl1]: 
    =Task2: [task ==> impl1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "impl1",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    hello
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "impl1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [sleep:  ]
    sleeping 1000 milli seconds
    ..........
      located task-> 3 [impl2]: 
    =Task3: [task ==> impl2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    world
    
```

##### Logs with different verbose level
* [c0087 log - verbose level v](../../logs/c0087_v)
* [c0087 log - verbose level vv](../../logs/c0087_vv)
* [c0087 log - verbose level vvv](../../logs/c0087_vvv)
* [c0087 log - verbose level vvvv](../../logs/c0087_vvvv)
* [c0087 log - verbose level vvvvv](../../logs/c0087_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0087)
