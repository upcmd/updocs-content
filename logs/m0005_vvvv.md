---
title: "0005_vvvv"
date: 2020-08-09T01:36:43+88:00
draft: false
weight: 100503

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0005/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0005
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0005
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0005
    -exec task: Main
    loading [Task]:  ./up.yml
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
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
    ~SubStep1: [inspect: the vars in caller before invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
    })
    
     2: inspect[exec_base_vars]
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb"
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
    module: [hello-module], instance id: [nonamed], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ nonamed ] runtime vars:
    {
      "a": "module-global-aaa",
      "c": "module-global-ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "module-global-ccc",
      "a": "module-global-aaa"
    }
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa"
    })
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "b": "caller-global-bbb",
      "d": "module-local-ddd",
      "a": "caller-global-aaa",
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
     1: inspect[exec_vars]
    (*core.Cache)({
      "d": "module-local-ddd",
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "up_runtime_tasker_layer_number": 2,
      "b": "caller-global-bbb"
    })
    
     2: inspect[exec_base_vars]
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "c": "module-global-ccc",
      "b": "caller-global-bbb"
    }
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .d "module-local-ddd"}}]
     5 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
    ~SubStep3: [return:  ]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "b": "caller-global-bbb",
      "c": "module-global-ccc",
      "e": "caller-global-eee",
      "a": "caller-global-aaa"
    })
    
     2: inspect[exec_base_vars]
    {
      "e": "caller-global-eee",
      "a": "caller-global-aaa",
      "b": "caller-global-bbb",
      "c": "module-global-ccc"
    }
    
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-global-aaa"}}]
     2 ASSERT OK:     [{{eq .b "caller-global-bbb"}}]
     3 ASSERT OK:     [{{eq .c "module-global-ccc"}}]
     4 ASSERT OK:     [{{eq .e "caller-global-eee"}}]
    
```

##### Logs with different verbose level
* [m0005 log - verbose level v](../../logs/m0005_v)
* [m0005 log - verbose level vv](../../logs/m0005_vv)
* [m0005 log - verbose level vvv](../../logs/m0005_vvv)
* [m0005 log - verbose level vvvv](../../logs/m0005_vvvv)
* [m0005 log - verbose level vvvvv](../../logs/m0005_vvvvv)

##### References
* [Related Chapter](../../module/0005)
