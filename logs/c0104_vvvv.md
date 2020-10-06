---
title: "c0104_vvvv"
date: 2020-10-07T00:11:17+1010:00
draft: false
weight: 11043

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0104
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
    loading [Task]:  ./tests/functests/c0104
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
      "extra_task_name": "post_task"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "extra_task_name": "post_task"
    })
    
      located task-> 4 [task]: 
    Task4: [task ==> task: this is the task and expect the final message (hello I love this world) ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "extra_task_name": "post_task",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "extra_task_name": "post_task"
    })
    
    cmd( 1):
    echo " I love this "
    
    cmd=>:
    echo " I love this "
    -
     I love this 
    
    -
     .. ok
    . ok
    -Step2: [: use a dynamic var to refer to a task name ]
    current exec runtime vars:
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [post_task]: 
    =Task2: [task ==> post_task: this is post-task ]
    Executing task stack layer: 2
    
    --Step1: [: do step1 in shell func ]
    current exec runtime vars:
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \" I love this \"",
        Code: 0,
        Output: "I love this",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "world"
    
    cmd=>:
    echo "world"
    -
    world
    
    -
     .. ok
    . ok
      located task-> 3 [2ndtask]: 
    =Task3: [task ==> 2ndtask:  ]
    Executing task stack layer: 2
    
    --Step1: [: to test multiple refs ]
    current exec runtime vars:
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "extra_task_name": "post_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"world\"",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "this is 2nd task"
    
    cmd=>:
    echo "this is 2nd task"
    -
    this is 2nd task
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0104 log - verbose level v](../../logs/c0104_v)
* [c0104 log - verbose level vv](../../logs/c0104_vv)
* [c0104 log - verbose level vvv](../../logs/c0104_vvv)
* [c0104 log - verbose level vvvv](../../logs/c0104_vvvv)
* [c0104 log - verbose level vvvvv](../../logs/c0104_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0104)
