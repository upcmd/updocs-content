---
title: "f0125_vvvv"
date: 2020-09-18T01:28:03+99:00
draft: false
weight: 11253

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0125
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/f0125
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
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    up_runtime_task_layer_number: 1
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    condition failed, skip executing step 
    
    ---Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2
    })
    
      located task-> 2 [layer2]: 
    ===Task2: [task/layer2/layer3 ==> layer2:  ]
    Executing task stack layer: 4
    
    ----Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
    ~~~~SubStep1: [print:  ]
    up_runtime_task_layer_number: 3
    ----Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 3
    })
    
      located task-> 3 [layer3]: 
    ====Task3: [task/layer2/layer3/layer2 ==> layer3:  ]
    Executing task stack layer: 5
    
    -----Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 4
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 4
    })
    
    ~~~~~SubStep1: [exit:  ]
      Exit: exit [client choose to exit]
    
```

##### Logs with different verbose level
* [f0125 log - verbose level v](../../logs/f0125_v)
* [f0125 log - verbose level vv](../../logs/f0125_vv)
* [f0125 log - verbose level vvv](../../logs/f0125_vvv)
* [f0125 log - verbose level vvvv](../../logs/f0125_vvvv)
* [f0125 log - verbose level vvvvv](../../logs/f0125_vvvvv)

##### References
* [Related Chapter](../../loop/f0125)
