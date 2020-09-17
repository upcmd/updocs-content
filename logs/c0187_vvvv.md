---
title: "c0187_vvvv"
date: 2020-09-18T01:27:57+99:00
draft: false
weight: 11873

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0187
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
    loading [Task]:  ./tests/functests/c0187
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
    
    -Step1: [: task ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
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
    
    ~~SubStep1: [print:  ]
    in sub_task_layer1
    --Step2: [: task ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item1",
      "loopindex": 0
    })
    
    --Step1: [: processing ..... ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa"
    })
    
    ~~SubStep1: [print:  ]
    aaaa
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
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
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
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
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
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
    --Step1: [: processing ..... ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb"
    })
    
    ~~SubStep1: [print:  ]
    bbbb
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
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
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
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
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
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
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    in sub_task_layer1
    --Step2: [: task ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "item2"
    })
    
    --Step1: [: processing ..... ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    aaaa
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "aaaa",
      "loopindex": 0
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
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
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
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
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy"
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
    --Step1: [: processing ..... ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    bbbb
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "bbbb"
    })
    
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: xxx"""
    -
    opening file: xxx
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
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
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "xxx",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      }),
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "xxx",
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
      located task-> 3 [sub_task_layer2]: 
    ==Task3: [task/sub_task_layer1 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 3
    
    ---Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: yyy"""
    -
    opening file: yyy
    
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
    ---Step2: [step2: in this case, since there is no ignoreError, the exception was captured by task level finaly code block
    opened file is safely closed
    to make the flow to continue to reach step2, use ignoreError
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello\"|grep \"world\"",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    ~~~SubStep1: [print:  ]
    step 2
    task Finally:
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "yyy",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "loopitem": "yyy",
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
* [c0187 log - verbose level v](../../logs/c0187_v)
* [c0187 log - verbose level vv](../../logs/c0187_vv)
* [c0187 log - verbose level vvv](../../logs/c0187_vvv)
* [c0187 log - verbose level vvvv](../../logs/c0187_vvvv)
* [c0187 log - verbose level vvvvv](../../logs/c0187_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0187)
