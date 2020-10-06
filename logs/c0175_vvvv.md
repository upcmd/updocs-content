---
title: "c0175_vvvv"
date: 2020-10-07T00:11:32+1010:00
draft: false
weight: 11753

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0175
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
    loading [Task]:  ./tests/functests/c0175
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
    Task1: [task ==> task: without rescue, the execution will return a non-zero  return code in shell and also report the error
    with rescue, the program will return 0
     ]
    Executing task stack layer: 1
    
    -Step1: [step1: step 1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "opening file"
    
    cmd=>:
    echo "opening file"
    -
    opening file
    
    -
     .. ok
    cmd( 2):
    echo "hello"|grep "world"
    
    cmd=>:
    echo "hello"|grep "world"
    -
    
    -
     .. failed(suppressed if it is not the last step)
    task Finally:
    -Step1: [
    close_fileensure the opened file is closed
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
     WARN: [Rescued in task level, but not advised!] - [setting rescue to yes/true to continue is not recommended
    it is advised to locate root cause of the problem, fix it and re-run the task again
    it is the best practice to test the execution in your ci pipeline to eliminate problems rather than dynamically fix using rescue]
    
```

##### Logs with different verbose level
* [c0175 log - verbose level v](../../logs/c0175_v)
* [c0175 log - verbose level vv](../../logs/c0175_vv)
* [c0175 log - verbose level vvv](../../logs/c0175_vvv)
* [c0175 log - verbose level vvvv](../../logs/c0175_vvvv)
* [c0175 log - verbose level vvvvv](../../logs/c0175_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0175)
