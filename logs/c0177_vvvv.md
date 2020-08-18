---
title: "c0177_vvvv"
date: 2020-08-18T15:16:25+88:00
draft: false
weight: 11773

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0177
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
    loading [Task]:  ./tests/functests/c0177
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
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "person": {
        "sex": "male",
        "age": 18,
        "name": "tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: this is a story about tom
     ]
    Executing task stack layer: 1
    
    -Step1: [: tom is male
     ]
    current exec runtime vars:
    (*core.Cache)({
      "school": "sydney grammar",
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      },
      "school": "sydney grammar"
    })
    
    ~SubStep1: [print: his age is 18
    he is in school: sydney grammar
     ]
    what gender is tom
    
```

##### Logs with different verbose level
* [c0177 log - verbose level v](../../logs/c0177_v)
* [c0177 log - verbose level vv](../../logs/c0177_vv)
* [c0177 log - verbose level vvv](../../logs/c0177_vvv)
* [c0177 log - verbose level vvvv](../../logs/c0177_vvvv)
* [c0177 log - verbose level vvvvv](../../logs/c0177_vvvvv)

##### References
* [Related Chapter](../../vars/c0177)
