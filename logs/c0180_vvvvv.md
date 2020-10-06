---
title: "c0180_vvvvv"
date: 2020-10-07T00:11:33+1010:00
draft: false
weight: 11804

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0180
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bd600)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e928)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: the output of cat would be silent ]
    {
      Name: "",
      Do: {
        "echo \"\"\"{{.msg}}\"\"\" > /tmp/msg",
        "cat /tmp/msg"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
      },
      Dvars: <nil>,
      Desc: "the output of cat would be silent",
      Reg: "",
      Flags: {
        "silent"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n",
      "up_runtime_task_layer_number": 0
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=64) "echo \"\"\"hello, world\nthank you\nhello tom\ngood buy\n\"\"\" > /tmp/msg",
     Code: (int) 0,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    cat /tmp/msg
    
    cmd=>:
    cat /tmp/msg
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "cat /tmp/msg",
     Code: (int) 0,
     Output: (string) (len=41) "hello, world\nthank you\nhello tom\ngood buy",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: explicitly show the the shell exec result ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.last_result.Output}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "explicitly show the the shell exec result",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      })
    })
    
    {{.last_result.Output}}
    ~SubStep1: [print:  ]
    hello, world
    thank you
    hello tom
    good buy
    -Step3: [: the silent will not affect output of failed shell execution ]
    {
      Name: "",
      Do: {
        ">&2 echo \"encountering an error\"\nexit -1\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
      },
      Dvars: <nil>,
      Desc: "the silent will not affect output of failed shell execution",
      Reg: "",
      Flags: {
        "silent",
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/msg",
        Code: 0,
        Output: "hello, world\nthank you\nhello tom\ngood buy",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg": "hello, world\nthank you\nhello tom\ngood buy\n"
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=41) ">&2 echo \"encountering an error\"\nexit -1\n",
     Code: (int) 2,
     Output: (string) "",
     ErrMsg: (string) (len=64) "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    -Step4: [
    silient only one sub step but not all
    in this case, it will make sub step 1 msg1 silent but not the msg2
    ]
    {
      Name: "",
      Do: {
        "echo \"\"\"{{.msg1}}\"\"\"",
        "echo \"\"\"{{.msg2}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "msg1": "sub step1",
        "msg2": "sub step2"
      },
      Dvars: <nil>,
      Desc: "silient only one sub step but not all\nin this case, it will make sub step 1 msg1 silent but not the msg2\n",
      Reg: "",
      Flags: {
        "silent-1"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: ">&2 echo \"encountering an error\"\nexit -1\n",
        Code: 2,
        Output: "",
        ErrMsg: "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
      }),
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1",
      "msg2": "sub step2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1",
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: ">&2 echo \"encountering an error\"\nexit -1\n",
        Code: 2,
        Output: "",
        ErrMsg: "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "msg1": "sub step1",
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: ">&2 echo \"encountering an error\"\nexit -1\n",
        Code: 2,
        Output: "",
        ErrMsg: "encountering an error\n/bin/sh: exit: line 2: Illegal number: -1\n"
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step1\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    sub step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step2\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step2",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step5: [
    silient only one sub step but not all
    in this case, it will make sub step 2 msg2 silent but not the msg1
    ]
    {
      Name: "",
      Do: {
        "echo \"\"\"{{.msg1}}\"\"\"",
        "echo \"\"\"{{.msg2}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "msg1": "sub step1",
        "msg2": "sub step2"
      },
      Dvars: <nil>,
      Desc: "silient only one sub step but not all\nin this case, it will make sub step 2 msg2 silent but not the msg1\n",
      Reg: "",
      Flags: {
        "silent-2"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "msg1": "sub step1",
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "msg1": "sub step1",
      "msg2": "sub step2",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    sub step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step1\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step2\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step2",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step6: [
    if there are combined flags of silent and silent-x, silent will take priority, then there will be no output for all of the sub steps
    ]
    {
      Name: "",
      Do: {
        "echo \"\"\"{{.msg1}}\"\"\"",
        "echo \"\"\"{{.msg2}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "msg2": "sub step2",
        "msg1": "sub step1"
      },
      Dvars: <nil>,
      Desc: "if there are combined flags of silent and silent-x, silent will take priority, then there will be no output for all of the sub steps\n",
      Reg: "",
      Flags: {
        "silent-1",
        "silent"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "msg1": "sub step1",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg2": "sub step2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "msg1": "sub step1",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"sub step2\"\"\"",
        Code: 0,
        Output: "sub step2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "msg2": "sub step2"
    }
    
    
    self: final context exec vars:
    
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
    
    cmd( 1):
    echo """{{.msg1}}"""
    
    cmd=>:
    echo """sub step1"""
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step1\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """{{.msg2}}"""
    
    cmd=>:
    echo """sub step2"""
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"\"\"sub step2\"\"\"",
     Code: (int) 0,
     Output: (string) (len=9) "sub step2",
     ErrMsg: (string) ""
    }
    
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
