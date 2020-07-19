---
title: "f0012_vvvv"
date: 2020-07-20T02:02:16+77:00
draft: false
weight: 101203

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 8
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/f0012
    -exec task: Main
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [hello-module] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [hello-module] task: [Say_hello]
    Executing tasker layer: 2
    
      located task-> 2 [Say_hello]: 
    Task2: [TODO: Main Caller Taskname ==> Say_hello:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [print:  ]
    ... hello
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk1] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Executing tasker layer: 3
    
      located task-> 3 [Cross_call1]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk2] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 4
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk1] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Executing tasker layer: 5
    
      located task-> 3 [Cross_call1]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk2] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 6
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk1] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Executing tasker layer: 7
    
      located task-> 3 [Cross_call1]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk2] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 8
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    ~SubStep1: [print:  ]
     .... cross call 2
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk1] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Executing tasker layer: 9
    
      ERROR: Module call layer check: [Too many layers of recursive module executions, max allowed(8), please fix your recursive call]
    
```

##### Logs with different verbose level
* [mf0012 log - verbose level v](../../logs/mf0012_v)
* [mf0012 log - verbose level vv](../../logs/mf0012_vv)
* [mf0012 log - verbose level vvv](../../logs/mf0012_vvv)
* [mf0012 log - verbose level vvvv](../../logs/mf0012_vvvv)
* [mf0012 log - verbose level vvvvv](../../logs/mf0012_vvvvv)

##### References
* [Related Chapter](../../module/f0012)
