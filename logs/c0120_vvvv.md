---
title: "c0120_vvvv"
date: 2020-08-18T15:16:12+88:00
draft: false
weight: 11203

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0120
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
    loading [Task]:  ./tests/functests/c0120
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
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    step1
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [break:  ]
    -Step3:
     WARN: [break] - [client chose to break]
    
```

##### Logs with different verbose level
* [c0120 log - verbose level v](../../logs/c0120_v)
* [c0120 log - verbose level vv](../../logs/c0120_vv)
* [c0120 log - verbose level vvv](../../logs/c0120_vvv)
* [c0120 log - verbose level vvvv](../../logs/c0120_vvvv)
* [c0120 log - verbose level vvvvv](../../logs/c0120_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0120)
