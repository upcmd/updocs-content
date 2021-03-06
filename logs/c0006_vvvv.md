---
title: "c0006_vvvv"
date: 2020-10-07T00:11:01+1010:00
draft: false
weight: 10063

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0006
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
    loading [Task]:  ./tests/functests/c0006
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
    
    -Step1: [: to test display env vars from shell context ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "aaa: $aaa"
    
    
    cmd=>:
    echo "aaa: $aaa"
    
    -
    aaa: 
    
    -
     .. ok
    cmd( 2):
    echo "bbb: $bbb"
    
    
    cmd=>:
    echo "bbb: $bbb"
    
    -
    bbb: 
    
    -
     .. ok
    cmd( 3):
    echo "aaa':' $aaa"
    
    cmd=>:
    echo "aaa':' $aaa"
    -
    aaa':' 
    
    -
     .. ok
    cmd( 4):
    echo "aaa":" $aaa"
    
    cmd=>:
    echo "aaa":" $aaa"
    -
    aaa: 
    
    -
     .. ok
    cmd( 5):
    echo "aaa -> $aaa"
    
    cmd=>:
    echo "aaa -> $aaa"
    -
    aaa -> 
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0006 log - verbose level v](../../logs/c0006_v)
* [c0006 log - verbose level vv](../../logs/c0006_vv)
* [c0006 log - verbose level vvv](../../logs/c0006_vvv)
* [c0006 log - verbose level vvvv](../../logs/c0006_vvvv)
* [c0006 log - verbose level vvvvv](../../logs/c0006_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0006)
