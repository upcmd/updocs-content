---
title: "c0163_vvvv"
date: 2020-08-09T01:36:25+88:00
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
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "aaa": "var_a_from_task"
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
    
    --Step1: [: inspect if the correct parameter has been passed in correctly
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
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Austraila",
      "loopindex1": 1,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Austraila",
      "loopindex1": 1,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "Austraila",
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"<=
    var_a_from_task
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Austraila"<=
    Austraila
     .. ok
    . ok
    --Step1: [: inspect if the correct parameter has been passed in correctly
    with default value
    in block func
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "US"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "US"
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"<=
    var_a_from_task
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "US"<=
    US
     .. ok
    . ok
    --Step1: [: inspect if the correct parameter has been passed in correctly
    with default value
    in block func
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      })
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
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopindex1": 3,
      "loopitem": "China",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopindex1": 3,
      "loopitem": "China",
      "loopindex": 2
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"<=
    var_a_from_task
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "China"<=
    China
     .. ok
    . ok
    --Step1: [: inspect if the correct parameter has been passed in correctly
    with default value
    in block func
     ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan",
      "loopindex": 3,
      "loopindex1": 4,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan"
    })
    
    cmd( 1):
    echo "{{.aaa}}"
    
    cmd=>:
    echo "var_a_from_task"<=
    var_a_from_task
     .. ok
    cmd( 2):
    echo "{{.loopitem}}"
    
    cmd=>:
    echo "Japan"<=
    Japan
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
