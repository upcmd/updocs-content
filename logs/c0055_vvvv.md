---
title: "c0055_vvvv"
date: 2020-09-18T01:27:29+99:00
draft: false
weight: 10553

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0055
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
    loading [Task]:  ./tests/functests/c0055
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    condition failed, skip executing step 
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    dvar> greet:
    "hello"
    
    -
    hello
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "greet": "hello"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [taska]: 
    =Task2: [task ==> taska:  ]
    Executing task stack layer: 2
    
    --Step1: [: greet var will be no value as it is a local var for cmd step ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "hello from taska"
    
    cmd=>:
    echo "hello from taska"
    -
    hello from taska
    
    -
     .. ok
    cmd( 2):
    echo "{{.greet}} from taska"
    
    cmd=>:
    echo "<no value> from taska"
    -
    <no value> from taska
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0055 log - verbose level v](../../logs/c0055_v)
* [c0055 log - verbose level vv](../../logs/c0055_vv)
* [c0055 log - verbose level vvv](../../logs/c0055_vvv)
* [c0055 log - verbose level vvvv](../../logs/c0055_vvvv)
* [c0055 log - verbose level vvvvv](../../logs/c0055_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0055)
