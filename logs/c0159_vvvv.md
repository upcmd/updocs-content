---
title: "c0159_vvvv"
date: 2020-10-07T00:11:29+1010:00
draft: false
weight: 11593

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0159
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
    loading [Task]:  ./tests/functests/c0159
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
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    test var overriding in sub_task
    ]
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    without default value
    ]
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    without default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step3: [
    inspect if the correct parameter has been passed in correctly
    with default value
    ]
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step4:
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    
```

##### Logs with different verbose level
* [c0159 log - verbose level v](../../logs/c0159_v)
* [c0159 log - verbose level vv](../../logs/c0159_vv)
* [c0159 log - verbose level vvv](../../logs/c0159_vvv)
* [c0159 log - verbose level vvvv](../../logs/c0159_vvvv)
* [c0159 log - verbose level vvvvv](../../logs/c0159_vvvvv)

##### References
* [Related Chapter](../../block-func/c0159)
