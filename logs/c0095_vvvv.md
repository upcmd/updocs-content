---
title: "c0095_vvvv"
date: 2020-09-18T01:27:36+99:00
draft: false
weight: 10953

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0095
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
    loading [Task]:  ./tests/functests/c0095
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
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n"
    })
    
    ~SubStep1: [toObj: the key is pointing to a var name and use its content as yml content
     ]
    ~SubStep2: [printObj:  ]
    (string) (len=13) "person_object"
    
    object:
     person_object: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    ~SubStep3: [print:  ]
    my name is: tom
    ~SubStep4: [toObj:  ]
    ~SubStep5: [printObj:  ]
    (string) (len=16) "{{.name_to_reg}}"
    
    object:
     person_dyna_object: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    ~SubStep6: [toObj: use src content directly ]
    ~SubStep7: [printObj:  ]
    (string) (len=16) "{{.name_to_reg}}"
    
    object:
     person_dyna_object: {
      "person": {
        "name": "jason",
        "age": 53
      }
    }
    
    
```

##### Logs with different verbose level
* [c0095 log - verbose level v](../../logs/c0095_v)
* [c0095 log - verbose level vv](../../logs/c0095_vv)
* [c0095 log - verbose level vvv](../../logs/c0095_vvv)
* [c0095 log - verbose level vvvv](../../logs/c0095_vvvv)
* [c0095 log - verbose level vvvvv](../../logs/c0095_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0095)
