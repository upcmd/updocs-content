---
title: "c0164_vvvv"
date: 2020-08-09T01:36:25+88:00
draft: false
weight: 11643

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0164
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
    loading [Task]:  ./tests/functests/c0164
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
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task"
    })
    
    ~SubStep1: [print:  ]
    [Austraila US China Japan]
    ~SubStep2: [typeOf:  ]
     1 -  type of [countries] > [[]interface {}]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
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
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "aaa": "var_a_from_task"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
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
    
    self: final context exec vars:
    
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
    
    --Step1: [: inspect if the correct parameter has been passed in correctly
    with default value
    in block func
     ]
    current exec runtime vars:
    (*core.Cache)({
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "Austraila"
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
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "Austraila"
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
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "Austraila"
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
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "loopitem": "Austraila"
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [assert:  ]
     1 ASSERT OK:     [{{eq .aaa "var_a_from_task"}}]
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Austraila\"",
        Code: 0,
        Output: "Austraila",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "US",
      "loopindex": 1,
      "loopindex1": 2
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3,
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"US\"",
        Code: 0,
        Output: "US",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "China",
      "loopindex": 2,
      "loopindex1": 3
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
      "loopindex1": 4,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan",
      "loopindex": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 4,
      "aaa": "var_a_from_task",
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "Japan",
      "loopindex": 3
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopindex1": 4,
      "loopitem": "Japan",
      "loopindex": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "countries": {
        "Austraila",
        "US",
        "China",
        "Japan"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"China\"",
        Code: 0,
        Output: "China",
        ErrMsg: ""
      }),
      "aaa": "var_a_from_task",
      "up_runtime_task_layer_number": 1,
      "loopindex1": 4,
      "loopitem": "Japan",
      "loopindex": 3
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
* [c0164 log - verbose level v](../../logs/c0164_v)
* [c0164 log - verbose level vv](../../logs/c0164_vv)
* [c0164 log - verbose level vvv](../../logs/c0164_vvv)
* [c0164 log - verbose level vvvv](../../logs/c0164_vvvv)
* [c0164 log - verbose level vvvvv](../../logs/c0164_vvvvv)

##### References
* [Related Chapter](../../block-func/c0164)
