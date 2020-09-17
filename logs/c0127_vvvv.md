---
title: "c0127_vvvv"
date: 2020-09-18T00:51:44+99:00
draft: false
weight: 11273

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0127
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
    loading [Task]:  ./tests/functests/c0127
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
      "goahead": false
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "goahead": false
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    false
    true
    
    -Step2: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "goahead": false
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    do something else .......
    -Step3: [: show example the else coud route to call a list of tasks ]
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    do something else .......
      located task-> 3 [goelse]: 
    =Task3: [task ==> goelse:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": false
    })
    
    ~~SubStep1: [print:  ]
    do something else .......
      located task-> 4 [goelse2]: 
    =Task4: [task ==> goelse2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": false
    })
    
    ~~SubStep1: [print:  ]
    do something else2 .......
      located task-> 4 [goelse2]: 
    =Task4: [task ==> goelse2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    do something else2 .......
    -Step4: [: show it is same that you could assemble a list of tasks for if true condition ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "goahead": true
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
      located task-> 2 [goahead]: 
    =Task2: [task ==> goahead:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": true,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    go ahead .......
    
```

##### Logs with different verbose level
* [c0127 log - verbose level v](../../logs/c0127_v)
* [c0127 log - verbose level vv](../../logs/c0127_vv)
* [c0127 log - verbose level vvv](../../logs/c0127_vvv)
* [c0127 log - verbose level vvvv](../../logs/c0127_vvvv)
* [c0127 log - verbose level vvvvv](../../logs/c0127_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0127)
