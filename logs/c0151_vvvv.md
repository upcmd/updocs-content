---
title: "c0151_vvvv"
date: 2020-10-06T23:46:19+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main task of hello world demo of UPcmd ]
    Executing task stack layer: 1
    
    -Step1: [: greet to Tom ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 0,
      "weather": "sunny"
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
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
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      }),
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Tom\"",
        Code: 0,
        Output: "Hello, Tom",
        ErrMsg: ""
      })
    })
    
    ~~SubStep1: [print:  ]
    What a great day!
    -Step2: [: greet to Grace ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "weather": "sunny"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "weather": "sunny",
      "greet_to": "Grace"
    })
    
      located task-> 2 [greet]: 
    =Task2: [task ==> greet: greet to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
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
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "weather": "sunny"
    })
    
    ~~SubStep1: [print:  ]
    It is sunny
    --Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "weather": "sunny"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Grace\"",
        Code: 0,
        Output: "Hello, Grace",
        ErrMsg: ""
      }),
      "weather": "sunny",
      "greet_to": "Grace",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    What a great day!
    -Step3: [: do  you get the idea? ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "weather": "sunny",
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "sunny",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [print:  ]
    Have you got a little taste of using the UPcmd?
    
    -Step4: [: greet to a team ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "weather": "stormy",
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "weather": "stormy",
      "greet_to": "Tom",
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
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Tom"
    })
    
    ~~SubStep1: [print:  ]
    Hi Jason, how are you?
    --Step2: [: greet to the team member ]
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason"
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason"
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
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Jason\"",
        Code: 0,
        Output: "Hello, Jason",
        ErrMsg: ""
      }),
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
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
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Jason",
      "loopindex": 0,
      "loopindex1": 1,
      "weather": "stormy",
      "greet_to": "Jason",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    ~~~SubStep1: [print:  ]
    What a bad day!!
      located task-> 3 [sayhi]: 
    =Task3: [task ==> sayhi: say hi to some one ]
    Executing task stack layer: 2
    
    --Step1: [: say hi to someone ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Tom",
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
      "weather": "stormy",
      "greet_to": "Tom",
      "up_runtime_task_layer_number": 1,
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
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 1,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
      located task-> 2 [greet]: 
    ==Task2: [task/sayhi ==> greet: greet to some one ]
    Executing task stack layer: 3
    
    ---Step1: [: say hello ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1
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
      "loopitem": "Connie",
      "loopindex": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Connie",
      "loopindex": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    ~~~SubStep1: [print:  ]
    It is stormy
    ---Step3: [: ice break ]
    current exec runtime vars:
    (*core.Cache)({
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "Connie",
      "loopindex": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"Hello, Connie\"",
        Code: 0,
        Output: "Hello, Connie",
        ErrMsg: ""
      }),
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      }
    })
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie",
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "team": {
        "Jason",
        "Connie"
      },
      "loopitem": "Connie",
      "loopindex": 1,
      "loopindex1": 2,
      "weather": "stormy",
      "greet_to": "Connie"
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
