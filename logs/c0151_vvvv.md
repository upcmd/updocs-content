---
title: "c0151_vvvv"
date: 2020-08-18T15:16:19+88:00
draft: false
weight: 11513

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0151
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
    loading [Task]:  ./tests/functests/c0151
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
      "greet_to": "Tom",
      "weather": "sunny"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "greet_to": "Tom",
      "weather": "sunny"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main task of hello world demo of UPcmd ]
    Executing task stack layer: 1
    
    -Step1: [: greet to Tom ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Tom"
    -
    Hello, Tom
    -
     .. ok
    . ok
    --Step2: [: talk about weather ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "sunny",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    What a great day!
    -Step2: [: greet to Grace ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Grace",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "greet_to": "Grace",
      "weather": "sunny"
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Grace",
      "weather": "sunny",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "greet_to": "Grace",
      "weather": "sunny"
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Grace"
    -
    Hello, Grace
    -
     .. ok
    . ok
    --Step2: [: talk about weather ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "greet_to": "Grace"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "greet_to": "Grace"
    })
    
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "greet_to": "Grace"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "greet_to": "Grace",
      "weather": "sunny"
    })
    
    ~~SubStep1: [print:  ]
    What a great day!
    -Step3: [: do  you get the idea? ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "up_runtime_task_layer_number": 1,
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "greet_to": "Tom",
      "weather": "sunny"
    })
    
    ~SubStep1: [print:  ]
    Have you got a little taste of using the UPcmd?
    
    -Step4: [: greet to a team ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
      located task-> 3 [sayhi]: 
    =Task3: [task ==> sayhi: say hi to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hi to someone ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Tom"
    })
    
    ~~SubStep1: [print:  ]
    Hi Jason, how are you?
    --Step2: [: greet to the team member ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason"
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Jason"
    -
    Hello, Jason
    -
     .. ok
    . ok
    ---Step2: [: talk about weather ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      })
    })
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "weather": "stormy"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "greet_to": "Jason",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      })
    })
    
    ~~~SubStep1: [print:  ]
    What a bad day!!
      located task-> 3 [sayhi]: 
    =Task3: [task ==> sayhi: say hi to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hi to someone ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1
    })
    
    ~~SubStep1: [print:  ]
    Hi Connie, how are you?
    --Step2: [: greet to the team member ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Tom",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    cmd( 1):
    echo "Hello, {{.greet_to}}"
    
    cmd=>:
    echo "Hello, Connie"
    -
    Hello, Connie
    -
     .. ok
    . ok
    ---Step2: [: talk about weather ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      })
    })
    
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "Connie",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie"
    })
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2,
      "greet_to": "Connie",
      "weather": "stormy"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Connie",
      "weather": "stormy",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~~SubStep1: [print:  ]
    What a bad day!!
    
```

##### Logs with different verbose level
* [c0151 log - verbose level v](../../logs/c0151_v)
* [c0151 log - verbose level vv](../../logs/c0151_vv)
* [c0151 log - verbose level vvv](../../logs/c0151_vvv)
* [c0151 log - verbose level vvvv](../../logs/c0151_vvvv)
* [c0151 log - verbose level vvvvv](../../logs/c0151_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0151)
