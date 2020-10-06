---
title: "c0059_vvvv"
date: 2020-10-06T23:46:00+1010:00
draft: false
weight: 10593

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0059
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
    loading [Task]:  ./tests/functests/c0059
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
    
    loading [flow ref]:  ./tests/functests/c0059-task-ref.yml
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
    
    cmd( 1):
    echo "step1"
    
    cmd=>:
    echo "step1"
    -
    step1
    
    -
     .. ok
    cmd( 2):
    echo "step2"
    
    cmd=>:
    echo "step2"
    -
    step2
    
    -
     .. ok
    cmd( 3):
    echo "step3"
    
    cmd=>:
    echo "step3"
    -
    step3
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "step4"
    
    cmd=>:
    echo "step4"
    -
    step4
    
    -
     .. ok
    cmd( 2):
    echo "step5"
    
    cmd=>:
    echo "step5"
    -
    step5
    
    -
     .. ok
    cmd( 3):
    echo "step6"
    
    cmd=>:
    echo "step6"
    -
    step6
    
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "step7"
    
    cmd=>:
    echo "step7"
    -
    step7
    
    -
     .. ok
    cmd( 2):
    echo "step8"
    
    cmd=>:
    echo "step8"
    -
    step8
    
    -
     .. ok
    cmd( 3):
    echo "step9"
    
    cmd=>:
    echo "step9"
    -
    step9
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0059 log - verbose level v](../../logs/c0059_v)
* [c0059 log - verbose level vv](../../logs/c0059_vv)
* [c0059 log - verbose level vvv](../../logs/c0059_vvv)
* [c0059 log - verbose level vvvv](../../logs/c0059_vvvv)
* [c0059 log - verbose level vvvvv](../../logs/c0059_vvvvv)

##### References
* [Related Chapter](../../organization/c0059)
