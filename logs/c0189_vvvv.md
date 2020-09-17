---
title: "c0189_vvvv"
date: 2020-09-18T01:27:58+99:00
draft: false
weight: 11893

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0189
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
    loading [Task]:  ./tests/functests/c0189
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
      "global_aa": "aa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "global_aa": "aa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 1
    
    -Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "local_bb": "bb",
      "task_tt": "tt"
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    . ok
    task Finally:
    Step1: [close_file: ensure the opened file is closed
     ]
    current exec runtime vars:
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "finally_cc": "cc"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_aa": "aa",
      "up_runtime_task_layer_number": 0,
      "task_tt": "tt",
      "finally_cc": "cc"
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
    
```

##### Logs with different verbose level
* [c0189 log - verbose level v](../../logs/c0189_v)
* [c0189 log - verbose level vv](../../logs/c0189_vv)
* [c0189 log - verbose level vvv](../../logs/c0189_vvv)
* [c0189 log - verbose level vvvv](../../logs/c0189_vvvv)
* [c0189 log - verbose level vvvvv](../../logs/c0189_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0189)
