---
title: "c0041_vvvv"
date: 2020-07-20T02:01:36+77:00
draft: false
weight: 10413

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0041
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0041
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
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hello
    
    cmd=>:
    echo hello<=
    hello
     .. ok
    cmd( 2):
    echo world
    
    cmd=>:
    echo world<=
    world
     .. ok
    . ok
    -Step2: [: step2 ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo tom
    
    cmd=>:
    echo tom<=
    tom
     .. ok
    cmd( 2):
    echo "{{.last_result.Code}}"
    
    cmd=>:
    echo "0"<=
    0
     .. ok
    cmd( 3):
    echo "{{.last_result.Output}}"
    
    cmd=>:
    echo "world"<=
    world
     .. ok
    cmd( 4):
    echo hanks
    
    cmd=>:
    echo hanks<=
    hanks
     .. ok
    . ok
    -Step3: [: step3 ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "greet": "hello: hanks\n"
    })
    
    cmd( 1):
    echo tom
    
    cmd=>:
    echo tom<=
    tom
     .. ok
    cmd( 2):
    echo "{{.last_result.Output}}"
    
    cmd=>:
    echo "hanks"<=
    hanks
     .. ok
    cmd( 3):
    echo hanks
    
    cmd=>:
    echo hanks<=
    hanks
     .. ok
    cmd( 4):
    echo "{{.greet}}"
    
    cmd=>:
    echo "hello: hanks
    "<=
    hello: hanks
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0041 log - verbose level v](../../logs/c0041_v)
* [c0041 log - verbose level vv](../../logs/c0041_vv)
* [c0041 log - verbose level vvv](../../logs/c0041_vvv)
* [c0041 log - verbose level vvvv](../../logs/c0041_vvvv)
* [c0041 log - verbose level vvvvv](../../logs/c0041_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0041)
