---
title: "c0108_vvvv"
date: 2020-09-18T01:27:39+99:00
draft: false
weight: 11083

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0108
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
    loading [Task]:  ./tests/functests/c0108
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
      "tom": "this is tom"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    this is tom
    ~SubStep2: [print:  ]
    this is jerry
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print: jerry is in local scope so there is no value ]
    None
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    ~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskScope ]
    this is jerry in task scope
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "jerry is overrided in local scope"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "jerry is overrided in local scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print: var jerry in task scope is overrided by local var jerry ]
    jerry is overrided in local scope
    -Step6:
    current exec runtime vars:
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "up_runtime_task_layer_number": 0,
      "jerry": "this is jerry in task scope"
    })
    
    ~SubStep1: [print: this should print out the jerry defined in task var scope ]
    this is jerry in task scope
    
```

##### Logs with different verbose level
* [c0108 log - verbose level v](../../logs/c0108_v)
* [c0108 log - verbose level vv](../../logs/c0108_vv)
* [c0108 log - verbose level vvv](../../logs/c0108_vvv)
* [c0108 log - verbose level vvvv](../../logs/c0108_vvvv)
* [c0108 log - verbose level vvvvv](../../logs/c0108_vvvvv)

##### References
* [Related Chapter](../../vars/c0108)
