---
title: "c0181_vvvv"
date: 2020-09-18T01:27:55+99:00
draft: false
weight: 11813

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0181
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
    loading [Task]:  ./tests/functests/c0181
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
    
    -Step1: [: break loop using until condition
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~SubStep1: [print:  ]
    item1
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~SubStep1: [print:  ]
    item2
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~SubStep1: [print:  ]
    item3
    loop util conditional break
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    ----------------------------------------------------
    -Step3: [: in this case the until condition will use a var which is chaning in block func
    in order to make the interal var accessible by parent block func, you will have to use return cmd to return the value, otherwise the block func can not use right changing value in the condition
    also the_internal_var has be be defined somewhere: scope/global/local, otherwise it will result in a golang templating error
     ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "None"
    })
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1",
      "loopitem": "item1"
    })
    
    ~SubStep1: [print:  ]
    item1
    ~SubStep2: [return:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "None"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~SubStep1: [print:  ]
    post process None to see if this is executed
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1",
      "loopitem": "item2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2",
      "loopitem": "item2"
    })
    
    ~SubStep1: [print:  ]
    item2
    ~SubStep2: [return:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1"
    })
    
    ~SubStep1: [print:  ]
    post process item1 to see if this is executed
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~SubStep1: [print:  ]
    item3
    ~SubStep2: [return:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    ~SubStep1: [print:  ]
    post process item2 to see if this is executed
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    ~SubStep1: [print:  ]
    item4
    ~SubStep2: [return:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopitem": "item4"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    ~SubStep1: [print:  ]
    post process item3 to see if this is executed
    loop util conditional break
    
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item4",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    ----------------------------------------------------
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "None"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "None"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item1",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    ~~SubStep1: [print:  ]
    item1
    ~~SubStep2: [return:  ]
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item2",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    ~~SubStep1: [print:  ]
    item2
    ~~SubStep2: [return:  ]
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item2",
      "loopitem": "item3"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item4",
      "the_internal_var2": "item3",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    item3
    ~~SubStep2: [return:  ]
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "the_internal_var2": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item4"
    })
    
    ~~SubStep1: [print:  ]
    item4
    ~~SubStep2: [return:  ]
    loop util conditional break
    
    -Step6:
    current exec runtime vars:
    (*core.Cache)({
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    
```

##### Logs with different verbose level
* [c0181 log - verbose level v](../../logs/c0181_v)
* [c0181 log - verbose level vv](../../logs/c0181_vv)
* [c0181 log - verbose level vvv](../../logs/c0181_vvv)
* [c0181 log - verbose level vvvv](../../logs/c0181_vvvv)
* [c0181 log - verbose level vvvvv](../../logs/c0181_vvvvv)

##### References
* [Related Chapter](../../loop/c0181)
