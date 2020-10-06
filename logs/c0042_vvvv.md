---
title: "c0042_vvvv"
date: 2020-10-06T23:45:57+1010:00
draft: false
weight: 10423

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0042
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
    loading [Task]:  ./tests/functests/c0042
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
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo tom
    
    cmd=>:
    echo tom
    -
    tom
    
    -
     .. ok
    cmd( 2):
    echo hanks
    
    cmd=>:
    echo hanks
    -
    hanks
    
    -
     .. ok
    . ok
    -Step2: [
    the last result of hanks will be registered as varname: hellomsg
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    dvar> reg_hello:
    "hello: hanks\n\n"
    
    -
    hello: hanks
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "hellomsg": "hanks",
      "reg_hello": "hello: hanks\n\n"
    })
    
    cmd( 1):
    echo "hellomsg  - {{.hellomsg}}"
    
    cmd=>:
    echo "hellomsg  - hanks"
    -
    hellomsg  - hanks
    
    -
     .. ok
    cmd( 2):
    echo "reg_hello - {{.reg_hello}}"
    
    cmd=>:
    echo "reg_hello - hello: hanks
    
    "
    -
    reg_hello - hello: hanks
    
    
    
    -
     .. ok
    . ok
    -Step3: [
    the hellomsg will be still availabe in this step
    it is removed but will be unavailabe in the next step
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"reg_hello - hello: hanks\n\n\"",
        Code: 0,
        Output: "reg_hello - hello: hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "reg_hello": "\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"reg_hello - hello: hanks\n\n\"",
        Code: 0,
        Output: "reg_hello - hello: hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
    cmd=>:
    echo "hanks"
    -
    hanks
    
    -
     .. ok
    . ok
    -Step4: [
    now the hellomsg should be <no value>
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
    cmd=>:
    echo "<no value>"
    -
    <no value>
    
    -
     .. ok
    . ok
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"<no value>\"",
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    dvar> void:
    "hello: something\n"
    
    -
    hello: something
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"<no value>\"",
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "iamvoid": "something"
    })
    
    cmd( 1):
    echo '{{.iamvoid}}'
    
    cmd=>:
    echo 'something'
    -
    something
    
    -
     .. ok
    . ok
    -Step6:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'something'",
        Code: 0,
        Output: "something",
        ErrMsg: ""
      }),
      "iamvoid": "something",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'something'",
        Code: 0,
        Output: "something",
        ErrMsg: ""
      }),
      "iamvoid": "something",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo '{{.iamvoid}}'
    
    cmd=>:
    echo 'something'
    -
    something
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0042 log - verbose level v](../../logs/c0042_v)
* [c0042 log - verbose level vv](../../logs/c0042_vv)
* [c0042 log - verbose level vvv](../../logs/c0042_vvv)
* [c0042 log - verbose level vvvv](../../logs/c0042_vvvv)
* [c0042 log - verbose level vvvvv](../../logs/c0042_vvvvv)

##### References
* [Related Chapter](../../object-oriented/c0042)
