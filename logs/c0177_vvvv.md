---
title: "c0177_vvvv"
date: 2020-10-06T23:46:25+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      },
      "env": "dev"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "person": {
        "age": 18,
        "name": "tom",
        "sex": "male"
      },
      "env": "dev"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: this is a story about tom
     ]
    Executing task stack layer: 1
    
    -Step1: [
    tom is male
    ]
    current exec runtime vars:
    (*core.Cache)({
      "person": {
        "age": 18,
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0,
      "school": "sydney grammar",
      "env": "dev"
    })
    
    Enter Value For [continue]: 
    Are you sure ? all items in dev infrastructure will be destroyed ! (yes/N)
    self: final context exec vars:
    
    (*core.Cache)({
      "continue": "N",
      "env": "dev",
      "person": {
        "age": 18,
        "name": "tom",
        "sex": "male"
      },
      "up_runtime_task_layer_number": 0,
      "school": "sydney grammar"
    })
    
    ~SubStep1: [print: his age is 18
    he is in school: sydney grammar
    ?continue: N
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
