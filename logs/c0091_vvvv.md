---
title: "c0091_vvvv"
date: 2020-10-07T00:11:15+1010:00
draft: false
weight: 10913

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0091
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
    loading [Task]:  ./tests/functests/c0091
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-tom
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-tom",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 0
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer2-peter",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopindex": 2
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-james
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-peter
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-peter",
      "loopindex": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "layer1-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0,
      "loopindex1": 1,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3,
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-james
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 2 [layer2]: 
    =Task2: [task ==> layer2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa"
    })
    
    ~~SubStep1: [print:  ]
    hello layer1-james
    ~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer1-james",
      "loopindex": 2
    })
    
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-tom",
      "loopindex": 0
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-tom
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa"
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-peter
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
      located task-> 3 [layer3]: 
    ==Task3: [task/layer2 ==> layer3:  ]
    Executing task stack layer: 3
    
    ---Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-james",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 2,
      "layer1_aaa": "layer1_aaa",
      "layer1_bbb": "layer1_bbb",
      "layer2_aaa": "layer2_aaa",
      "layer2_bbb": "layer2_bbb",
      "loopitem": "layer2-james"
    })
    
    ~~~SubStep1: [print:  ]
    hello layer2-james
    ~~~SubStep2: [print:  ]
    hello layer1_aaa: layer1_aaa
    ~~~SubStep3: [print:  ]
    hello layer2_aaa: layer2_aaa
    
```

##### Logs with different verbose level
* [c0091 log - verbose level v](../../logs/c0091_v)
* [c0091 log - verbose level vv](../../logs/c0091_vv)
* [c0091 log - verbose level vvv](../../logs/c0091_vvv)
* [c0091 log - verbose level vvvv](../../logs/c0091_vvvv)
* [c0091 log - verbose level vvvvv](../../logs/c0091_vvvvv)

##### References
* [Related Chapter](../../loop/c0091)
