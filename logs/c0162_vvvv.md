---
title: "c0162_vvvv"
date: 2020-08-18T15:16:22+88:00
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "who_is_trusted": "my_friend",
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "my_friend": "joe doe"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "who_is_trusted": "my_friend",
      "friends": {
        "tom",
        "jane",
        "hans",
        "coook"
      },
      "my_friend": "joe doe",
      "countries": "- Austraila\n- US\n- China\n- Japan\n"
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
      "my_friend": "john"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
