---
title: "c0113_vvvv"
date: 2020-10-07T00:11:19+1010:00
draft: false
weight: 11133

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0113
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
    loading [Task]:  ./tests/functests/c0113
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
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: call subtask and exam the return value in following steps ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom after it is registered in current task stack ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func1",
      "tom": "this is tom in global"
    })
    
    ~~SubStep1: [reg: by default hitom is registered in to global context ]
    ~~SubStep2: [print:  ]
    in sub_loop print1: tom created in sub_loop
    ~~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    --Step2: [: check value of tom and it should be available in current stack ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "tom created in sub_loop",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2",
      "tom": "tom created in sub_loop",
      "jerry": "this is jerry in global"
    })
    
    ~~SubStep1: [print:  ]
    in sub_loop print2: tom created in sub_loop
    ~~SubStep2: [assert: since .tom is in callee's global, it should be accessible here ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    ~~SubStep3: [return: it should return and merge tom to parent's vars scope
    it should report warning as jason does not exist
     ]
     WARN: [return validation] - [The referencing var name: (jason) not exist]
    -Step2: [: check value of tom ]
    current exec runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in sub_loop"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in sub_loop",
      "jerry": "this is jerry in global"
    })
    
    ~SubStep1: [print:  ]
    in main task print3: tom created in sub_loop
    ~SubStep2: [assert: since .tom is returned from callee, it should be accessible here ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    
```

##### Logs with different verbose level
* [c0113 log - verbose level v](../../logs/c0113_v)
* [c0113 log - verbose level vv](../../logs/c0113_vv)
* [c0113 log - verbose level vvv](../../logs/c0113_vvv)
* [c0113 log - verbose level vvvv](../../logs/c0113_vvvv)
* [c0113 log - verbose level vvvvv](../../logs/c0113_vvvvv)

##### References
* [Related Chapter](../../call-func/c0113)
