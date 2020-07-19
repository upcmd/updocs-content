---
title: "0006_vvvv"
date: 2020-07-20T02:02:15+77:00
draft: false
weight: 100603

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0006/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0006
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0006
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0006
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
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    ~SubStep1: [inspect: the vars in caller before invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
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
      "a": "module-global-aaa",
      "c": "module-global-ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "module-global-aaa",
      "c": "module-global-ccc"
    }
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [inspect: the result would be:
    a: caller-global-aaa
    b: caller-global-bbb
    c: module-global-ccc
    d: module-local-ddd
    e: caller-global-eee
     ]
     1: inspect[exec_vars](*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "e": "caller-global-eee"
    }
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .d "module-local-ddd"}}]
     5 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
    ~SubStep3: [return:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "i": "module-local-call-iii",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "h": "module-local-call-hhh"
    })
    
      located task-> 3 [second_layer_internal_call]: 
    =Task3: [TODO: Main Caller Taskname/Say_world ==> second_layer_internal_call:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "i": "module-local-call-iii",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb",
      "h": "module-local-call-hhh",
      "d": "module-local-call-ddd"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb",
      "i": "module-local-call-iii",
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh"
    })
    
    ~~SubStep1: [inspect: second_layer_internal_call
    a: module-local-call-aaa
    b: module-local-call-bbb
    d: module-local-call-ddd
     ]
     1: inspect[exec_vars](*core.Cache)({
      "d": "module-local-call-ddd",
      "h": "module-local-call-hhh",
      "up_runtime_task_layer_number": 1,
      "b": "caller-global-bbb",
      "i": "module-local-call-iii",
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "up_runtime_tasker_layer_number": 2
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "d": "module-local-call-ddd",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "h": "module-local-call-hhh",
      "i": "module-local-call-iii"
    }
    
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .d "module-local-call-ddd"}}]
     5 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
     6 ASSERT OK:     [{{eq .i "module-local-call-iii"}}]
     7 ASSERT OK:     [{{eq .h "module-local-call-hhh"}}]
     8 ASSERT OK:     [{{eq .k "module-second_layer_local-kkk"}}]
    ~~SubStep3: [return:  ]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "k": "module-second_layer_local-kkk"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 1,
      "k": "module-second_layer_local-kkk",
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb"
    })
    
    ~SubStep1: [return: var k is return from second_layer_internal_call ]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk",
      "up_runtime_task_layer_number": 1,
      "up_runtime_tasker_layer_number": 2
    })
    
     2: inspect[exec_base_vars]{
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "e": "caller-global-eee",
      "c": "module-global-ccc",
      "k": "module-second_layer_local-kkk"
    }
    
    ~SubStep2: [assert: note the k is the result from the 2nd layer call
     ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
     5 ASSERT OK:     [{{eq .k "module-second_layer_local-kkk"}}]
    
```

##### Logs with different verbose level
* [m0006 log - verbose level v](../../logs/m0006_v)
* [m0006 log - verbose level vv](../../logs/m0006_vv)
* [m0006 log - verbose level vvv](../../logs/m0006_vvv)
* [m0006 log - verbose level vvvv](../../logs/m0006_vvvv)
* [m0006 log - verbose level vvvvv](../../logs/m0006_vvvvv)

##### References
* [Related Chapter](../../module/0006)
