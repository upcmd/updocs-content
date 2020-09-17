---
title: "c0114_vvvv"
date: 2020-09-18T01:27:40+99:00
draft: false
weight: 11143

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0114
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
    loading [Task]:  ./tests/functests/c0114
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
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: call subtask and exam the return value in following steps ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global",
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom after it is registered in current task stack ]
    current exec runtime vars:
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "jerry": "this is jerry in global",
      "tom": "this is tom in global",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "jerry": "this is jerry in global",
      "tom": "this is tom in global",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [reg: by default hitom is registered in to global context ]
    ~~SubStep2: [print:  ]
    in sub_loop print1: tom created in subtask1
    --Step2: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    in sub_loop print2: tom created in subtask1
    ~~SubStep2: [return:  ]
    --Step3: [: call subtask and exam the return value in following steps ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1"
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
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global",
      "john": "john in sub_loop func1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 2,
      "jerry": "this is jerry in global"
    })
    
    ~~~SubStep1: [reg: by default hitom is registered in to global context ]
    ~~~SubStep2: [print:  ]
    in sub_loop print1: tom2 created in subtask2
    ---Step2: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "tom": "tom2 created in subtask2",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    in sub_loop print2: tom2 created in subtask2
    ~~~SubStep2: [return:  ]
    -Step2: [: check value of tom
    in this case tom's value should come from subtask1
    tom's expected value:  tom created in subtask1
     ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in subtask1",
      "up_runtime_task_layer_number": 2
    })
    
    ~SubStep1: [print:  ]
    in main task print3: tom created in subtask1
    
```

##### Logs with different verbose level
* [c0114 log - verbose level v](../../logs/c0114_v)
* [c0114 log - verbose level vv](../../logs/c0114_vv)
* [c0114 log - verbose level vvv](../../logs/c0114_vvv)
* [c0114 log - verbose level vvvv](../../logs/c0114_vvvv)
* [c0114 log - verbose level vvvvv](../../logs/c0114_vvvvv)

##### References
* [Related Chapter](../../call-func/c0114)
