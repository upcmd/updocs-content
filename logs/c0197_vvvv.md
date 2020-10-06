---
title: "c0197_vvvv"
date: 2020-10-06T23:46:28+1010:00
draft: false
weight: 11973

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0197
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
    loading [Task]:  ./tests/functests/c0197
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
      "enc_key": "my_enc_key",
      "up_runtime_task_layer_number": 0
    })
    
    dvar> value_encrypted:
    "y76l464966iQdDOawpQCwLjx6+ZPqnyj7O8x1MUtpsU="
    
    -
    y76l464966iQdDOawpQCwLjx6+ZPqnyj7O8x1MUtpsU=
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_AAA": "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM=",
      "envVar_ENV_AAA": "ENV_AAA",
      "value_encrypted": "y76l464966iQdDOawpQCwLjx6+ZPqnyj7O8x1MUtpsU=",
      "ENV_BBB": "I_AM_ENV_VAR_BBB",
      "up_runtime_task_layer_number": 0,
      "enc_key": "my_enc_key",
      "envVar_ENV_BBB": "I_AM_ENV_VAR_BBB"
    })
    
    cmd( 1):
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: {{.secure_ENV_AAA}}"""
    
    
    cmd=>:
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: SECURE_SENSITIVE_INFO_MASKED"""
    
    -
    normal env var: I_AM_ENV_VAR_BBB
    expected decrypted secure env var: ENV_AAA
    normal secure var: ENV_AAA
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0197 log - verbose level v](../../logs/c0197_v)
* [c0197 log - verbose level vv](../../logs/c0197_vv)
* [c0197 log - verbose level vvv](../../logs/c0197_vvv)
* [c0197 log - verbose level vvvv](../../logs/c0197_vvvv)
* [c0197 log - verbose level vvvvv](../../logs/c0197_vvvvv)

##### References
* [Related Chapter](../../security/c0197)
