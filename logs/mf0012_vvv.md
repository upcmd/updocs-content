---
title: "f0012_vvv"
date: 2020-09-18T00:52:29+99:00
draft: false
weight: 101202

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/f0012/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/f0012
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/f0012
                TaskFile -> up.yml
                 Verbose -> vvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 8
               EntryTask -> Main
    work dir: /up_project/up/tests/modtests/f0012
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    Task1: [Main ==> Main: main entry ]
    -Step1:
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [hello-module] task: [Say_hello]
    Task2: [TODO: Main Caller Taskname ==> Say_hello:  ]
    -Step1:
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2,
      "a": "aaa"
    })
    
    ~SubStep1: [print:  ]
    ... hello
    -Step2:
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    -Step1:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 3
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 3
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    -Step1:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    -Step1:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    -Step1:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    -Step1:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    -Step1:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 8
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    =>call module: [crosstalk1] task: [Cross_call1]
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally -> runtime error: invalid memory address or nil pointer dereference
    
```

##### Logs with different verbose level
* [mf0012 log - verbose level v](../../logs/mf0012_v)
* [mf0012 log - verbose level vv](../../logs/mf0012_vv)
* [mf0012 log - verbose level vvv](../../logs/mf0012_vvv)
* [mf0012 log - verbose level vvvv](../../logs/mf0012_vvvv)
* [mf0012 log - verbose level vvvvv](../../logs/mf0012_vvvvv)

##### References
* [Related Chapter](../../module/f0012)
