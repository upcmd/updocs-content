---
title: "c0103_vvvv"
date: 2020-07-20T02:01:47+77:00
draft: false
weight: 11033

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0103
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0103
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
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: inplace modification ]
    current exec runtime vars:
    (*core.Cache)({
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    })
    
    ~SubStep1: [ymlWrite:  ]
    ~SubStep2: [print:  ]
    tom:
      sex: female
      age: 23
    
    ~SubStep3: [ymlWrite:  ]
    ~SubStep4: [print:  ]
    tom:
      sex: female
      age: 23
      wife:
        emily:
          sex: female
          age: 32
    
    
```

##### Logs with different verbose level
* [c0103 log - verbose level v](../../logs/c0103_v)
* [c0103 log - verbose level vv](../../logs/c0103_vv)
* [c0103 log - verbose level vvv](../../logs/c0103_vvv)
* [c0103 log - verbose level vvvv](../../logs/c0103_vvvv)
* [c0103 log - verbose level vvvvv](../../logs/c0103_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0103)
