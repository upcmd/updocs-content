---
title: "c0135_vvvv"
date: 2020-08-18T15:16:15+88:00
draft: false
weight: 11353

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0135
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
    loading [Task]:  ./tests/functests/c0135
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
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
      located task-> 2 [task]: 
    Task2: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa"
    })
    
      located task-> 1 [callee_task]: 
    =Task1: [task ==> callee_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "callee_db",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da"
    })
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "callee_db"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "callee_db",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 1
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: callee_db
    
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "local_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "callee_db" }}]
    
```

##### Logs with different verbose level
* [c0135 log - verbose level v](../../logs/c0135_v)
* [c0135 log - verbose level vv](../../logs/c0135_vv)
* [c0135 log - verbose level vvv](../../logs/c0135_vvv)
* [c0135 log - verbose level vvvv](../../logs/c0135_vvvv)
* [c0135 log - verbose level vvvvv](../../logs/c0135_vvvvv)

##### References
* [Related Chapter](../../block-func/c0135)
