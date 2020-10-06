---
title: "0009_vvvv"
date: 2020-10-06T23:46:55+1010:00
draft: false
weight: 100903

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0009/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0009
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0009
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0009
    -exec task: Main
    loading [Task]:  ./up.yml
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
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [m0009 log - verbose level v](../../logs/m0009_v)
* [m0009 log - verbose level vv](../../logs/m0009_vv)
* [m0009 log - verbose level vvv](../../logs/m0009_vvv)
* [m0009 log - verbose level vvvv](../../logs/m0009_vvvv)
* [m0009 log - verbose level vvvvv](../../logs/m0009_vvvvv)

##### References
* [Related Chapter](../../module/0009)
