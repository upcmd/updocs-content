---
title: "f0172_vvvv"
date: 2020-09-18T00:52:03+99:00
draft: false
weight: 11723

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0172
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
    loading [Task]:  ./tests/functests/f0172
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
    
    -Step1: [: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    step 1
    ~SubStep2: [panic:  ]
     WARN: [manual panic] - [manual trigger a panic cmd]
    Step Finally:
    Recovered from: manual trigger a panic cmd
      located task-> 2 [close_file]: 
    =Task2: [task ==> close_file:  ]
    Executing task stack layer: 2
    
    --Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 1
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
     WARN: [Not rescued in step level] - [please assess the panic problem and cause, fix it before re-run the task]
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally -> manual trigger a panic cmd
    
```

##### Logs with different verbose level
* [f0172 log - verbose level v](../../logs/f0172_v)
* [f0172 log - verbose level vv](../../logs/f0172_vv)
* [f0172 log - verbose level vvv](../../logs/f0172_vvv)
* [f0172 log - verbose level vvvv](../../logs/f0172_vvvv)
* [f0172 log - verbose level vvvvv](../../logs/f0172_vvvvv)

##### References
* [Related Chapter](../../flow-controll/f0172)
