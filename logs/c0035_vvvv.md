---
title: "c0035_vvvv"
date: 2020-07-20T02:01:35+77:00
draft: false
weight: 10353

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0035
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0035
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [step1:  ]
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb"
    })
    
    cmd( 1):
    pwd
    
    cmd=>:
    pwd<=
    /up_project/up
     .. ok
    . ok
    -Step2: [step2:  ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.a}}"
    
    cmd=>:
    echo "<no value>"<=
    <no value>
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0035 log - verbose level v](../../logs/c0035_v)
* [c0035 log - verbose level vv](../../logs/c0035_vv)
* [c0035 log - verbose level vvv](../../logs/c0035_vvv)
* [c0035 log - verbose level vvvv](../../logs/c0035_vvvv)
* [c0035 log - verbose level vvvvv](../../logs/c0035_vvvvv)

##### References
* [Related Chapter](../../vars/c0035)
