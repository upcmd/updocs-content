---
title: "c0132_vvvv"
date: 2020-10-07T00:11:23+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0132
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
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "block_layer2_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "block_layer2_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    })
    
    ~SubStep1: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
     2 ASSERT OK:     [{{eq .a "block_layer2_aaa"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT FAILED: [{{eq .a "aaa"}}]
    ~SubStep3: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "a": "block_layer2_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
     2: inspect[exec_base_vars]
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
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
