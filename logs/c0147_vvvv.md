---
title: "c0147_vvvv"
date: 2020-10-06T23:46:19+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "c": "ccc",
      "a": "aaa",
      "b": "bbb-global"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "b": "bbb-global",
      "c": "ccc",
      "a": "aaa"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "d": "ddd"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "d": "ddd"
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "d": "ddd"
    })
    
     2: inspect[exec_base_vars]
    {
      "c": "ccc",
      "a": "aaa",
      "b": "bbb-global"
    }
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .b  "bbb"}}]
     2 ASSERT OK:     [{{eq .d  "ddd"}}]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "f": "first_level_fff",
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "f": "first_level_fff",
      "e": "first_level_eee"
    })
    
      located task-> 2 [substack]: 
    =Task2: [task ==> substack:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "e": "first_level_eee"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "e": "first_level_eee"
    })
    
    ~~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "g": "ggg",
      "h": "hhh",
      "f": "first_level_fff",
      "e": "first_level_eee",
      "up_runtime_task_layer_number": 1
    })
    
     2: inspect[exec_base_vars]
    {
      "up_runtime_task_layer_number": 0,
      "f": "first_level_fff",
      "e": "first_level_eee"
    }
    
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .f  "first_level_fff"}}]
     2 ASSERT OK:     [{{eq .e  "first_level_eee"}}]
     3 ASSERT OK:     [{{eq .g  "ggg"}}]
    
```

##### Logs with different verbose level
* [c0147 log - verbose level v](../../logs/c0147_v)
* [c0147 log - verbose level vv](../../logs/c0147_vv)
* [c0147 log - verbose level vvv](../../logs/c0147_vvv)
* [c0147 log - verbose level vvvv](../../logs/c0147_vvvv)
* [c0147 log - verbose level vvvvv](../../logs/c0147_vvvvv)

##### References
* [Related Chapter](../../vars/c0147)
