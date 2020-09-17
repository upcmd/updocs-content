---
title: "c0183_vvvv"
date: 2020-09-18T01:27:56+99:00
draft: false
weight: 11833

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0183
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
    loading [Task]:  ./tests/functests/c0183
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: expect sub_task to close file each time in loop iteration
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 2
    
    --Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": 1,
      "loopindex": 0
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": 1,
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    step 2
    task Finally:
    -Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": 1,
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."
    -
    close the file .....
    
    -
     .. ok
    . ok
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 2
    
    --Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    --Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    step 2
    task Finally:
    -Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": 2,
      "loopindex": 1
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."
    -
    close the file .....
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0183 log - verbose level v](../../logs/c0183_v)
* [c0183 log - verbose level vv](../../logs/c0183_vv)
* [c0183 log - verbose level vvv](../../logs/c0183_vvv)
* [c0183 log - verbose level vvvv](../../logs/c0183_vvvv)
* [c0183 log - verbose level vvvvv](../../logs/c0183_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0183)
