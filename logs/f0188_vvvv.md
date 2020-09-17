---
title: "f0188_vvvv"
date: 2020-09-18T01:28:05+99:00
draft: false
weight: 11883

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0188
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
    loading [Task]:  ./tests/functests/f0188
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
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    case item1
    --Step2: [step1: conditionall trigger the error ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    condition failed, skip executing step step1
    
    --Step3: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1"
    })
    
    ~~SubStep1: [print:  ]
    step 2
    task Finally:
    -Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1"
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
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    case item2
    --Step2: [step1: conditionall trigger the error ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
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
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    echo "case {{.loopitem}} "
    
    cmd=>:
    echo "case item2 "
    -
    case item2 
    
    -
     .. ok
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
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
     WARN: [Rescued in task level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
      located task-> 2 [sub_task]: 
    ==Task2: [task/sub_task ==> sub_task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "item3",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "item3",
      "loopindex": 2
    })
    
    ~~~SubStep1: [print:  ]
    case item3
    ---Step2: [step1: conditionall trigger the error ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2
    })
    
    condition failed, skip executing step step1
    
    ---Step3: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "loopitem": "item3"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "loopitem": "item3"
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
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    
```

##### Logs with different verbose level
* [f0188 log - verbose level v](../../logs/f0188_v)
* [f0188 log - verbose level vv](../../logs/f0188_vv)
* [f0188 log - verbose level vvv](../../logs/f0188_vvv)
* [f0188 log - verbose level vvvv](../../logs/f0188_vvvv)
* [f0188 log - verbose level vvvvv](../../logs/f0188_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0188)
