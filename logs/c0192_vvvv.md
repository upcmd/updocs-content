---
title: "c0192_vvvv"
date: 2020-10-07T00:11:34+1010:00
draft: false
weight: 11923

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0192
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
    loading [Task]:  ./tests/functests/c0192
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
      "global_aa": "aa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "global_aa": "aa"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: loop through test cases ]
    current exec runtime vars:
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt",
      "global_aa": "aa"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0
    })
    
    cmd( 1):
    echo "main task start"
    
    cmd=>:
    echo "main task start"
    -
    main task start
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [cc]: 
    =Task2: [task ==> cc:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa"
    })
    
    cmd( 1):
    echo "in cc ...."
    
    cmd=>:
    echo "in cc ...."
    -
    in cc ....
    
    -
     .. ok
    . ok
    task Finally:
    -Step1: [
    close_fileensure the opened file is closed
    ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "global_aa": "aa",
      "finally_cc": "cc",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "finally_cc": "cc",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "close the file {{.loopitem}}"
    
    cmd=>:
    echo "close the file item1"
    -
    close the file item1
    
    -
     .. ok
    . ok
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "local_bb": "bb",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "loopitem": "item2",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "local_bb": "bb",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "loopitem": "item2"
    })
    
    cmd( 1):
    echo "main task start"
    
    cmd=>:
    echo "main task start"
    -
    main task start
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
      located task-> 2 [cc]: 
    =Task2: [task ==> cc:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "global_aa": "aa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"main task start\"",
        Code: 0,
        Output: "main task start",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt"
    })
    
    cmd( 1):
    echo "in cc ...."
    
    cmd=>:
    echo "in cc ...."
    -
    in cc ....
    
    -
     .. ok
    . ok
    task Finally:
    -Step1: [
    close_fileensure the opened file is closed
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "finally_cc": "cc",
      "global_aa": "aa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "local_bb": "bb",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "finally_cc": "cc"
    })
    
    cmd( 1):
    echo "close the file {{.loopitem}}"
    
    cmd=>:
    echo "close the file item2"
    -
    close the file item2
    
    -
     .. ok
    . ok
    task Finally:
    Step1:
    current exec runtime vars:
    (*core.Cache)({
      "task_tt": "tt",
      "finally_task": "ff",
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 1,
      "task_tt": "tt",
      "finally_task": "ff"
    })
    
    cmd( 1):
    echo "main task final"
    
    cmd=>:
    echo "main task final"
    -
    main task final
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0192 log - verbose level v](../../logs/c0192_v)
* [c0192 log - verbose level vv](../../logs/c0192_vv)
* [c0192 log - verbose level vvv](../../logs/c0192_vvv)
* [c0192 log - verbose level vvvv](../../logs/c0192_vvvv)
* [c0192 log - verbose level vvvvv](../../logs/c0192_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0192)
