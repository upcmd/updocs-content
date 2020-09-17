---
title: "c0197_vvvv"
date: 2020-09-18T01:28:00+99:00
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
      "enc_key": "my_enc_key"
    })
    
    dvar> value_encrypted:
    "YGufc3GdQOBHVL4RY5UVPN4OW1uOTCciHiSnJ3ITPok="
    
    -
    YGufc3GdQOBHVL4RY5UVPN4OW1uOTCciHiSnJ3ITPok=
    self: final context exec vars:
    
    (*core.Cache)({
      "envVar_ENV_BBB": "I_AM_ENV_VAR_BBB",
      "ENV_AAA": "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM=",
      "secure_ENV_AAA": "ENV_AAA",
      "envVar_ENV_AAA": "ENV_AAA",
      "up_runtime_task_layer_number": 0,
      "enc_key": "my_enc_key",
      "value_encrypted": "YGufc3GdQOBHVL4RY5UVPN4OW1uOTCciHiSnJ3ITPok=",
      "ENV_BBB": "I_AM_ENV_VAR_BBB"
    })
    
    cmd( 1):
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: {{.secure_ENV_AAA}}"""
    
    
    cmd=>:
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: ENV_AAA"""
    
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
