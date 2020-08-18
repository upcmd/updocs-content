---
title: "c0112_vvvv"
date: 2020-08-18T15:16:10+88:00
draft: false
weight: 11123

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0112
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
    loading [Task]:  ./tests/functests/c0112
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
      "global_a": "aaa",
      "global_b": "bbb"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "global_a": "aaa",
      "global_b": "bbb"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa"
    })
    
    ~~SubStep1: [print:  ]
    my name is tom
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "global_b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    })
    
    ~~SubStep1: [print:  ]
    my name is tom
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    --Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa"
    })
    
      located task-> 3 [subtask2]: 
    ==Task3: [task/subtask1 ==> subtask2:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 2,
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa"
    })
    
    ~~~SubStep1: [print:  ]
    my name is tom
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    ---Step2:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "local_a": "aaa",
      "local_b": "bbb",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    my name is tom
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    
```

##### Logs with different verbose level
* [c0112 log - verbose level v](../../logs/c0112_v)
* [c0112 log - verbose level vv](../../logs/c0112_vv)
* [c0112 log - verbose level vvv](../../logs/c0112_vvv)
* [c0112 log - verbose level vvvv](../../logs/c0112_vvvv)
* [c0112 log - verbose level vvvvv](../../logs/c0112_vvvvv)

##### References
* [Related Chapter](../../call-func/c0112)
