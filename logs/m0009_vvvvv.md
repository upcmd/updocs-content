---
title: "0009_vvvvv"
date: 2020-10-07T00:12:04+1010:00
draft: false
weight: 100904

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0009
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175ba0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b68a8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
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
