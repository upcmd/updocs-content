---
title: "c0115_vvvv"
date: 2020-08-18T15:16:11+88:00
draft: false
weight: 11153

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0115
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0115
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
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [main task: call subtask and exam the return value in following steps ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom after it is registered in current task stack ]
    current exec runtime vars:
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    ~~SubStep1: [reg: by default hitom is registered in to global context ]
    ~~SubStep2: [print:  ]
    in subtask1 print1: tom created in subtask1
    --Step2: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "john": "john in sub_loop func2",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global"
    })
    
    ~~SubStep1: [print:  ]
    in subtask1 print21: tom created in subtask1
    --Step3: [: call subtask and exam the return value in following steps ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in global"
    })
    
      located task-> 3 [subtask2]: 
    ==Task3: [task/subtask1 ==> subtask2: subtask to test reg and return ]
    Executing task stack layer: 3
    
    ---Step1: [: check value of tom after it is registered in current task stack ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "john": "john in sub_loop func1",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1"
    })
    
    ~~~SubStep1: [reg: by default hitom is registered in to global context ]
    ~~~SubStep2: [print:  ]
    in subtask2 print1: tom2 created in subtask2
    ---Step2: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global"
    })
    
    ~~~SubStep1: [print:  ]
    in subtask2 print2: tom2 created in subtask2
    ~~~SubStep2: [return:  ]
      located task-> 4 [subtask3]: 
    ==Task4: [task/subtask1 ==> subtask3: subtask3 ]
    Executing task stack layer: 3
    
    ---Step1: [: dummy ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global",
      "tom": "tom2 created in subtask2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    dummy to help build inspect task
    --Step4: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2"
    })
    
    ~~SubStep1: [print:  ]
    in subtask1 print22: tom2 created in subtask2
    ~~SubStep2: [return:  ]
    -Step2: [: check value of tom
    in this case tom's value should come from subtask1
    tom's expected value:  tom created in subtask1
     ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2
    })
    
    ~SubStep1: [print:  ]
    in main task print3: tom2 created in subtask2
    
```

##### Logs with different verbose level
* [c0115 log - verbose level v](../../logs/c0115_v)
* [c0115 log - verbose level vv](../../logs/c0115_vv)
* [c0115 log - verbose level vvv](../../logs/c0115_vvv)
* [c0115 log - verbose level vvvv](../../logs/c0115_vvvv)
* [c0115 log - verbose level vvvvv](../../logs/c0115_vvvvv)

##### References
* [Related Chapter](../../call-func/c0115)
