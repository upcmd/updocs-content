---
title: "c0013_vvvv"
date: 2020-09-18T00:51:21+99:00
draft: false
weight: 10133

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0013
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
    loading [Task]:  ./tests/functests/c0013
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
      "e": "runtime-e",
      "k": "runtime-k",
      "studentname": "Jason",
      "a": "runtime-a"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "studentname": "Jason",
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [step1: to test display env vars from shell context ]
    current exec runtime vars:
    (*core.Cache)({
      "studentname": "Tom",
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 0,
      "school": "SG"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 0,
      "school": "SG",
      "studentname": "Tom",
      "a": "runtime-a"
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"
    -
    hello, world
    
    -
     .. ok
    cmd( 2):
    echo "hello {{.studentname}}"
    
    cmd=>:
    echo "hello Tom"
    -
    hello Tom
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0013 log - verbose level v](../../logs/c0013_v)
* [c0013 log - verbose level vv](../../logs/c0013_vv)
* [c0013 log - verbose level vvv](../../logs/c0013_vvv)
* [c0013 log - verbose level vvvv](../../logs/c0013_vvvv)
* [c0013 log - verbose level vvvvv](../../logs/c0013_vvvvv)

##### References
* [Related Chapter](../../vars/c0013)
