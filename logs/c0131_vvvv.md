---
title: "c0131_vvvv"
date: 2020-10-07T00:11:23+1010:00
draft: false
weight: 11313

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0131
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
    loading [Task]:  ./tests/functests/c0131
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
      "goahead": false
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "goahead": false
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
    true
    
    -Step2: [: show use a flow in else ]
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    do something else step1 .......
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "goahead": false
    })
    
    cmd( 1):
    echo do something else step2 .......
    
    cmd=>:
    echo do something else step2 .......
    -
    do something else step2 .......
    
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    do something else step3 .......
    -Step4: [: show it is same that you could assemble a list of tasks for if true condition ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "goahead": true
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo do something else step2 .......",
        Code: 0,
        Output: "do something else step2 .......",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    ~~SubStep1: [print:  ]
    do something else .......
    
```

##### Logs with different verbose level
* [c0131 log - verbose level v](../../logs/c0131_v)
* [c0131 log - verbose level vv](../../logs/c0131_vv)
* [c0131 log - verbose level vvv](../../logs/c0131_vvv)
* [c0131 log - verbose level vvvv](../../logs/c0131_vvvv)
* [c0131 log - verbose level vvvvv](../../logs/c0131_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0131)
