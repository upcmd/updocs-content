---
title: "c0203_vvvv"
date: 2020-10-06T23:46:29+1010:00
draft: false
weight: 12033

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0203
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
    loading [Task]:  ./tests/functests/c0203
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
      "up_runtime_task_layer_number": 0
    })
    
    dvar> value_encrypted:
    "NA0bw54h5dBrEuqPAUumT12Z37nAXxGGQdKBs6W/SDk="
    
    -
    NA0bw54h5dBrEuqPAUumT12Z37nAXxGGQdKBs6W/SDk=
    self: final context exec vars:
    
    (*core.Cache)({
      "value_encrypted": "NA0bw54h5dBrEuqPAUumT12Z37nAXxGGQdKBs6W/SDk=",
      "ENV_AAA": "NA0bw54h5dBrEuqPAUumT12Z37nAXxGGQdKBs6W/SDk=",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello, this is a secrt value: {{.secure_ENV_AAA}}"
    
    cmd=>:
    echo "hello, this is a secrt value: SECURE_SENSITIVE_INFO_MASKED"
    -
    hello, this is a secrt value: ENV_AAA
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0203 log - verbose level v](../../logs/c0203_v)
* [c0203 log - verbose level vv](../../logs/c0203_vv)
* [c0203 log - verbose level vvv](../../logs/c0203_vvv)
* [c0203 log - verbose level vvvv](../../logs/c0203_vvvv)
* [c0203 log - verbose level vvvvv](../../logs/c0203_vvvvv)

##### References
* [Related Chapter](../../security/c0203)
