---
title: "0003_vvvv"
date: 2020-10-07T00:12:02+1010:00
draft: false
weight: 100303

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0003/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0003
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0003
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0003
    -exec task: Main
    loading [Task]:  ./up.yml
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
      "a": "caller-aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "caller-aaa"
    })
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "up_runtime_task_layer_number": 0
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    ... module world
    a: caller-aaa
    b: module-bbb
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    ~SubStep3: [return: var b should be return to caler
     ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
     2: inspect[exec_base_vars]
    {
      "a": "caller-aaa",
      "b": "module-bbb"
    }
    
    ~SubStep2: [print:  ]
    back to main caller
    a: caller-aaa
    b: module-bbb
    
    ~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    
```

##### Logs with different verbose level
* [m0003 log - verbose level v](../../logs/m0003_v)
* [m0003 log - verbose level vv](../../logs/m0003_vv)
* [m0003 log - verbose level vvv](../../logs/m0003_vvv)
* [m0003 log - verbose level vvvv](../../logs/m0003_vvvv)
* [m0003 log - verbose level vvvvv](../../logs/m0003_vvvvv)

##### References
* [Related Chapter](../../module/0003)
