---
title: "c0132_vvvv"
date: 2020-07-20T02:01:53+77:00
draft: false
weight: 11323

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0132
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0132
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
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db"
    })
    
    ~SubStep1: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
     2 ASSERT OK:     [{{eq .a "block_layer2_aaa"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
    ~SubStep3: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "b": "local_bbb",
      "da": "local_da"
    })
    
     2: inspect[exec_base_vars]{
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    }
    
    
```

##### Logs with different verbose level
* [c0132 log - verbose level v](../../logs/c0132_v)
* [c0132 log - verbose level vv](../../logs/c0132_vv)
* [c0132 log - verbose level vvv](../../logs/c0132_vvv)
* [c0132 log - verbose level vvvv](../../logs/c0132_vvvv)
* [c0132 log - verbose level vvvvv](../../logs/c0132_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0132)
