---
title: "c0162_vvvv"
date: 2020-10-07T00:11:29+1010:00
draft: false
weight: 11623

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0162
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
    loading [Task]:  ./tests/functests/c0162
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
      "my_friend": "joe doe",
      "who_is_trusted": "my_friend",
      "up_runtime_task_layer_number": 0,
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "my_friend": "joe doe",
      "who_is_trusted": "my_friend",
      "countries": "- Austraila\n- US\n- China\n- Japan\n",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    - Austraila
    - US
    - China
    - Japan
    
    ~SubStep2: [typeOf:  ]
     1 -  type of [countries] > [string]
     2 -  type of [friends] > [[]interface {}]
     3 -  type of [my_friend] > [string]
     4 -  type of [my_friend] > [string]
    ~SubStep3: [print:  ]
    type of countries: string
    type of friends: []interface {}
    type of my_friends: string
    who is trusted: string
    
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "my_friend": "john"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "my_friend": "john"
    })
    
    ~SubStep1: [print:  ]
    hello: john
    
```

##### Logs with different verbose level
* [c0162 log - verbose level v](../../logs/c0162_v)
* [c0162 log - verbose level vv](../../logs/c0162_vv)
* [c0162 log - verbose level vvv](../../logs/c0162_vvv)
* [c0162 log - verbose level vvvv](../../logs/c0162_vvvv)
* [c0162 log - verbose level vvvvv](../../logs/c0162_vvvvv)

##### References
* [Related Chapter](../../template/c0162)
