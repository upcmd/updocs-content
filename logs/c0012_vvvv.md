---
title: "c0012_vvvv"
date: 2020-08-18T15:15:49+88:00
draft: false
weight: 10123

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0012
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
    loading [Task]:  ./tests/functests/c0012
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
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: to test display env vars from shell context ]
    current exec runtime vars:
    (*core.Cache)({
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"
    -
    hello, world
    -
     .. ok
    cmd( 2):
    echo 'hello {{.a}}'
    
    cmd=>:
    echo 'hello runtime-a'
    -
    hello runtime-a
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0012 log - verbose level v](../../logs/c0012_v)
* [c0012 log - verbose level vv](../../logs/c0012_vv)
* [c0012 log - verbose level vvv](../../logs/c0012_vvv)
* [c0012 log - verbose level vvvv](../../logs/c0012_vvvv)
* [c0012 log - verbose level vvvvv](../../logs/c0012_vvvvv)

##### References
* [Related Chapter](../../vars/c0012)
