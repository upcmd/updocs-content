---
title: "c0180_vvvv"
date: 2020-10-07T00:11:33+1010:00
draft: false
weight: 11803

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0180
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
    loading [Task]:  ./tests/functests/c0180
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
    
    -Step1: [: the output of cat would be silent ]
    current exec runtime vars:
    (*core.Cache)({
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
    })
    
    cmd( 1):
    echo """{{.msg}}""" > /tmp/msg
    
    cmd=>:
    echo """hello, world
    thank you
    hello tom
    good buy
    """ > /tmp/msg
    -
    
    -
     .. ok
    cmd( 2):
    cat /tmp/msg
    
    cmd=>:
    cat /tmp/msg
    -
    
    -
     .. ok
    . ok
    -Step2: [: explicitly show the the shell exec result ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    hello, world
    thank you
    hello tom
    good buy
    -Step3: [: the silent will not affect output of failed shell execution ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
    })
    
    cmd( 1):
    >&2 echo "encountering an error"
    exit -1
    
    
    cmd=>:
    >&2 echo "encountering an error"
    exit -1
    
    -
    encountering an error
    /bin/sh: exit: line 2: Illegal number: -1
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step4: [
    silient only one sub step but not all
    in this case, it will make sub step 1 msg1 silent but not the msg2
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "msg2": "sub step2",
      "msg1": "sub step1",
      "last_result": (*utils.ExecResult)({
        Cmd: ">&2 echo \"encountering an error\"\nexit -1\n",
        Code: 2,
        Output: "",
        ErrMsg: "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: ">&2 echo \"encountering an error\"\nexit -1\n",
        Code: 2,
        Output: "",
        ErrMsg: "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
      }),
      "up_runtime_task_layer_number": 0,
      "msg2": "sub step2",
      "msg1": "sub step1"
    })
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    
    -
     .. ok
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    sub step2
    
    -
     .. ok
    . ok
    -Step5: [
    silient only one sub step but not all
    in this case, it will make sub step 2 msg2 silent but not the msg1
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg2": "sub step2",
      "msg1": "sub step1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "msg2": "sub step2",
      "msg1": "sub step1",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    sub step1
    
    -
     .. ok
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    
    -
     .. ok
    . ok
    -Step6: [
    if there are combined flags of silent and silent-x, silent will take priority, then there will be no output for all of the sub steps
    ]
    current exec runtime vars:
    (*core.Cache)({
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1",
      "msg2": "sub step2"
    })
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    
    -
     .. ok
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0180 log - verbose level v](../../logs/c0180_v)
* [c0180 log - verbose level vv](../../logs/c0180_vv)
* [c0180 log - verbose level vvv](../../logs/c0180_vvv)
* [c0180 log - verbose level vvvv](../../logs/c0180_vvvv)
* [c0180 log - verbose level vvvvv](../../logs/c0180_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0180)
