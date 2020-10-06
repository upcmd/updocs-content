---
title: "c0202_vvvv"
date: 2020-10-07T00:11:36+1010:00
draft: false
weight: 12023

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0202
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
    loading [Task]:  ./tests/functests/c0202
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
    })
    
    
    global: (*core.Cache)({
    })
    
    
    groups members:[dev]
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
    "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw="
    
    -
    Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_AAA": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=",
      "value_encrypted": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    var: Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=
    decrypted secure var: ENV_AAA
    
    ~SubStep2: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "ENV_AAA": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=",
      "secure_ENV_AAA": "ENV_AAA",
      "value_encrypted": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw="
    })
    
     2: inspect[exec_base_vars]
    {
    }
    
     3: inspect[exec_base_env_vars_configured]
     4: inspect[exec_env_vars_configured]
     5: inspect[debug_vars]
    -debug vars-
    "UpRunTimeVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    "RuntimeVarsAndDvarsMerged"
    (*core.Cache)({
    })
    
    "ExecbaseVars"
    (*core.Cache)({
    })
    
    "TaskVars"
    (*core.Cache)({
      "value_encrypted": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw="
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "ENV_AAA": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw=",
      "secure_ENV_AAA": "ENV_AAA",
      "value_encrypted": "Ac7HsDc+/d9lrMs8YBdPbT61DTZPHovNj6zN5d93ZGw="
    })
    
    --
    
```

##### Logs with different verbose level
* [c0202 log - verbose level v](../../logs/c0202_v)
* [c0202 log - verbose level vv](../../logs/c0202_vv)
* [c0202 log - verbose level vvv](../../logs/c0202_vvv)
* [c0202 log - verbose level vvvv](../../logs/c0202_vvvv)
* [c0202 log - verbose level vvvvv](../../logs/c0202_vvvvv)

##### References
* [Related Chapter](../../security/c0202)
