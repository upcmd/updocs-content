---
title: "c0147_vvvv"
date: 2020-08-18T15:16:19+88:00
draft: false
weight: 11473

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0147
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
    loading [Task]:  ./tests/functests/c0147
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
      "b": "bbb",
      "c": "ccc",
      "a": "aaa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "b": "bbb",
      "c": "ccc",
      "a": "aaa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "b": "bbb",
      "d": "ddd"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "d": "ddd",
      "b": "bbb"
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "b": "bbb",
      "d": "ddd"
    })
    
     2: inspect[exec_base_vars]
    {
      "c": "ccc",
      "a": "aaa",
      "b": "bbb"
    }
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .b  "bbb"}}]
     2 ASSERT OK:     [{{eq .d  "ddd"}}]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "e": "first_level_eee",
      "f": "first_level_fff"
    })
    
      located task-> 2 [substack]: 
    =Task2: [task ==> substack:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "f": "first_level_fff",
      "g": "ggg",
      "h": "hhh",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "e": "first_level_eee",
      "f": "first_level_fff",
      "g": "ggg",
      "h": "hhh",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "f": "first_level_fff",
      "g": "ggg",
      "h": "hhh",
      "up_runtime_task_layer_number": 1,
      "e": "first_level_eee"
    })
    
     2: inspect[exec_base_vars]
    {
      "e": "first_level_eee",
      "f": "first_level_fff"
    }
    
    
```

##### Logs with different verbose level
* [c0147 log - verbose level v](../../logs/c0147_v)
* [c0147 log - verbose level vv](../../logs/c0147_vv)
* [c0147 log - verbose level vvv](../../logs/c0147_vvv)
* [c0147 log - verbose level vvvv](../../logs/c0147_vvvv)
* [c0147 log - verbose level vvvvv](../../logs/c0147_vvvvv)

##### References
* [Related Chapter](../../vars/c0147)
