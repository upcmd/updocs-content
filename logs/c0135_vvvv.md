---
title: "c0135_vvvv"
date: 2020-07-20T02:01:53+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0135
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
    
      located task-> 2 [task]: 
    Task2: [task ==> task:  ]
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db"
    })
    
      located task-> 1 [callee_task]: 
    =Task1: [task ==> callee_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 1,
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "up_runtime_task_layer_number": 1,
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "callee_db",
      "da": "local_da"
    })
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "callee_db",
      "da": "local_da",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "callee_db",
      "da": "local_da",
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
