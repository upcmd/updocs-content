---
title: "c0173_vvvv"
date: 2020-10-07T00:11:31+1010:00
draft: false
weight: 11733

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0173
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
    loading [Task]:  ./tests/functests/c0173
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
      "global_aaa": "aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "global_aaa": "aaa"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "global_aaa": "aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_aaa": "local_aaa",
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    step 1
    ~SubStep2: [panic:  ]
     WARN: [manual panic] - [manual trigger a panic cmd]
    Step Finally:
    Recovered from: manual trigger a panic cmd
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa"
    })
    
    ~SubStep1: [print:  ]
    global aaa: aaa
    ~SubStep2: [print:  ]
    local aaa: local_aaa
    -Step2: [
    close_fileensure the opened file is closed
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "close the file ....."
    
    cmd=>:
    echo "close the file ....."
    -
    close the file .....
    
    -
     .. ok
    . ok
    -Step3: [: extra steps ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "local_aaa": "local_aaa",
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    ~SubStep1: [print:  ]
    extra step
     WARN: [Rescued in step level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    -Step2: [: step 2 ]
    current exec runtime vars:
    (*core.Cache)({
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aaa": "aaa",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"close the file .....\"",
        Code: 0,
        Output: "close the file .....",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    step 2
    
```

##### Logs with different verbose level
* [c0173 log - verbose level v](../../logs/c0173_v)
* [c0173 log - verbose level vv](../../logs/c0173_vv)
* [c0173 log - verbose level vvv](../../logs/c0173_vvv)
* [c0173 log - verbose level vvvv](../../logs/c0173_vvvv)
* [c0173 log - verbose level vvvvv](../../logs/c0173_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0173)
