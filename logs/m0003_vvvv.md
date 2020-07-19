---
title: "0003_vvvv"
date: 2020-07-20T02:02:15+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0003
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
      "a": "caller-aaa"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "caller-aaa"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa"
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
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
      "up_runtime_tasker_layer_number": 2
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2
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
      "up_runtime_tasker_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "b": "module-bbb",
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-aaa"
    })
    
     2: inspect[exec_base_vars]{
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
