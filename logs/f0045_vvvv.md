---
title: "f0045_vvvv"
date: 2020-08-09T01:36:28+88:00
draft: false
weight: 10453

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0045
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
    loading [Task]:  ./tests/functests/f0045
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
          template rendering -> template: .:1:23: executing "." at <validateMandatoryFailIfNone "student_name">: error calling validateMandatoryFailIfNone:   ERROR: validateMandatoryFailIfNone [Required var:(student_name) must not be empty, please fix it]
    
    WARN:
        1:{{ env "STUDENT_NAME" |validateMandatoryFailIfNone "student_name" }}
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    ---------group vars----------
    
    global: {
      "student_name": "None"
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student_name": "None"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student_name": "None"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [f0045 log - verbose level v](../../logs/f0045_v)
* [f0045 log - verbose level vv](../../logs/f0045_vv)
* [f0045 log - verbose level vvv](../../logs/f0045_vvv)
* [f0045 log - verbose level vvvv](../../logs/f0045_vvvv)
* [f0045 log - verbose level vvvvv](../../logs/f0045_vvvvv)

##### References
* [Related Chapter](../../env-vars/f0045)
