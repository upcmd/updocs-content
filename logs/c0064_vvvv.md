---
title: "c0064_vvvv"
date: 2020-09-18T00:51:29+99:00
draft: false
weight: 10643

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0064
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
    loading [Task]:  ./tests/functests/c0064
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello 1"
    
    cmd=>:
    echo "hello 1"
    -
    hello 1
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello 1\"",
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    ~SubStep1: [print: print some info ]
    hello, this is print commmand
    ~SubStep2: [print:  ]
    hello, Sydney Grammar
    ~SubStep3: [print:  ]
    hello, Sydney Grammar
    hello, Sydney Grammar
    
    
```

##### Logs with different verbose level
* [c0064 log - verbose level v](../../logs/c0064_v)
* [c0064 log - verbose level vv](../../logs/c0064_vv)
* [c0064 log - verbose level vvv](../../logs/c0064_vvv)
* [c0064 log - verbose level vvvv](../../logs/c0064_vvvv)
* [c0064 log - verbose level vvvvv](../../logs/c0064_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0064)
