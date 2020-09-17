---
title: "f0186_vvvv"
date: 2020-09-18T00:52:04+99:00
draft: false
weight: 11863

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0186
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
    loading [Task]:  ./tests/functests/f0186
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
      "loopindex1": 1,
      "loopitem": "item1",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopindex1": 1,
      "loopitem": "item1",
      "loopindex": 0
    })
    
      located task-> 2 [sub_task_layer1]: 
    =Task2: [task ==> sub_task_layer1: sub_task_layer1 ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "item1",
      "loopindex": 0
    })
    
    ~~SubStep1: [print:  ]
    in sub_task_layer1
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1,
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
      "loopitem": "aaa",
      "loopindex": 0,
      "up_runtime_task_layer_number": 2,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "loopitem": "aaa",
      "loopindex": 0,
      "up_runtime_task_layer_number": 2
    })
    
    cmd( 1):
    echo """opening file: {{.loopitem}}"""
    
    cmd=>:
    echo """opening file: aaa"""
    -
    opening file: aaa
    
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
    ---Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "up_runtime_task_layer_number": 2,
      "loopindex1": 1,
      "loopitem": "aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "up_runtime_task_layer_number": 2,
      "loopindex1": 1,
      "loopitem": "aaa"
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
      located task-> 3 [sub_task_layer2]: 
    ===Task3: [task/sub_task_layer1/sub_task_layer2 ==> sub_task_layer2: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 4
    
    ----Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "loopitem": "bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "up_runtime_task_layer_number": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "up_runtime_task_layer_number": 3,
      "loopindex1": 2,
      "loopitem": "bbb",
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
    echo """opening file: bbb"""
    -
    opening file: bbb
    
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
    ----Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 3,
      "loopindex1": 2,
      "loopitem": "bbb",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "up_runtime_task_layer_number": 3,
      "loopindex1": 2,
      "loopitem": "bbb"
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
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally ->   ERROR: Failed And Not Ignored! [You may want to continue and ignore the error]
    
    
```

##### Logs with different verbose level
* [f0186 log - verbose level v](../../logs/f0186_v)
* [f0186 log - verbose level vv](../../logs/f0186_vv)
* [f0186 log - verbose level vvv](../../logs/f0186_vvv)
* [f0186 log - verbose level vvvv](../../logs/f0186_vvvv)
* [f0186 log - verbose level vvvvv](../../logs/f0186_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0186)