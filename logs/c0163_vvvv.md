---
title: "c0163_vvvv"
date: 2020-10-07T00:11:30+1010:00
draft: false
weight: 11633

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0163
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
    loading [Task]:  ./tests/functests/c0163
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
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    dvar> countries:
    "- Austraila\n- US\n- China\n- Japan\n"
    
    -
    - Austraila
    - US
    - China
    - Japan
    
    dvar[object]> countries:
    {
      "Austraila",
      "US",
      "China",
      "Japan"
    }
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 0,
      "aaa": "var_a_from_task"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1
    })
    
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "aaa": "var_a_from_task"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Austraila",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Austraila"
    -
    Austraila
    
    -
     .. ok
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "US"
    -
    US
    
    -
     .. ok
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopindex1": 3,
      "loopitem": "China",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "China",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopindex1": 3
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
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
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "China"
    -
    China
    
    -
     .. ok
    . ok
    --Step1: [
    inspect if the correct parameter has been passed in correctly
    with default value
    in block func
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"
    -
    var_a_from_task
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Japan"
    -
    Japan
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0163 log - verbose level v](../../logs/c0163_v)
* [c0163 log - verbose level vv](../../logs/c0163_vv)
* [c0163 log - verbose level vvv](../../logs/c0163_vvv)
* [c0163 log - verbose level vvvv](../../logs/c0163_vvvv)
* [c0163 log - verbose level vvvvv](../../logs/c0163_vvvvv)

##### References
* [Related Chapter](../../block-func/c0163)
