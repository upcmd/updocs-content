---
title: "c0136_vvvv"
date: 2020-08-18T15:16:16+88:00
draft: false
weight: 11363

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0136
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
    loading [Task]:  ./tests/functests/c0136
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
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
      located task-> 3 [callee_task1]: 
    =Task3: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1",
      "a": "local_aaa"
    })
    
      located task-> 2 [callee_task2]: 
    ==Task2: [task/callee_task1 ==> callee_task2:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "a": "local_aaa",
      "db": "local_db_callee_task1",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "a": "local_aaa",
      "db": "callee_db_callee_task2",
      "b": "local_bbb"
    })
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 2,
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da_callee_task1
    db: callee_db_callee_task2
    
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "local_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da_callee_task1" }}]
     5 ASSERT OK:     [{{eq .db "callee_db_callee_task2" }}]
    
```

##### Logs with different verbose level
* [c0136 log - verbose level v](../../logs/c0136_v)
* [c0136 log - verbose level vv](../../logs/c0136_vv)
* [c0136 log - verbose level vvv](../../logs/c0136_vvv)
* [c0136 log - verbose level vvvv](../../logs/c0136_vvvv)
* [c0136 log - verbose level vvvvv](../../logs/c0136_vvvvv)

##### References
* [Related Chapter](../../block-func/c0136)
