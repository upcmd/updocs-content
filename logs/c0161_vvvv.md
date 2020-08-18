---
title: "c0161_vvvv"
date: 2020-08-18T15:16:22+88:00
draft: false
weight: 11613

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0161
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
    loading [Task]:  ./tests/functests/c0161
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
    
    -Step1: [: test var overriding in sub_task
     ]
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
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
    
    --Step1: [: inspect if the correct parameter has been passed in correctly
    with default value
    in block func
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
    --Step2:
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
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0161 log - verbose level v](../../logs/c0161_v)
* [c0161 log - verbose level vv](../../logs/c0161_vv)
* [c0161 log - verbose level vvv](../../logs/c0161_vvv)
* [c0161 log - verbose level vvvv](../../logs/c0161_vvvv)
* [c0161 log - verbose level vvvvv](../../logs/c0161_vvvvv)

##### References
* [Related Chapter](../../block-func/c0161)
