---
title: "c0025_vvvv"
date: 2020-10-07T00:11:04+1010:00
draft: false
weight: 10253

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0025
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
    loading [Task]:  ./tests/functests/c0025
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
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
    cmd=>:
    echo """a smart guy=>name: "Tom"
    sex: "Male"
    school: "Sydney Grammar"
    """
    -
    a smart guy=>name: Tom
    sex: Male
    school: Sydney Grammar
    
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0025 log - verbose level v](../../logs/c0025_v)
* [c0025 log - verbose level vv](../../logs/c0025_vv)
* [c0025 log - verbose level vvv](../../logs/c0025_vvv)
* [c0025 log - verbose level vvvv](../../logs/c0025_vvvv)
* [c0025 log - verbose level vvvvv](../../logs/c0025_vvvvv)

##### References
* [Related Chapter](../../dvars/c0025)
