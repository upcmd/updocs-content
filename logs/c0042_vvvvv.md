---
title: "c0042_vvvvv"
date: 2020-10-06T23:45:57+1010:00
draft: false
weight: 10424

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
    loading [Task]:  ./tests/functests/c0042
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c15e0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e938)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    {
      Name: "",
      Do: {
        "echo tom",
        "echo hanks"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step1",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=8) "echo tom",
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo hanks
    
    cmd=>:
    echo hanks
    -
    hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hanks",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [
    the last result of hanks will be registered as varname: hellomsg
    ]
    {
      Name: "",
      Do: {
        "echo \"hellomsg  - {{.hellomsg}}\"",
        "echo \"reg_hello - {{.reg_hello}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "reg_hello",
          Value: "hello: {{.last_result.Output|reg \"hellomsg\" }}\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "the last result of hanks will be registered as varname: hellomsg\n",
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
    
    
    [local] dvar expanded result:
    {
      "hellomsg": "hanks",
      "reg_hello": "hello: hanks\n\n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "reg_hello": "hello: hanks\n\n",
      "hellomsg": "hanks"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "reg_hello": "hello: hanks\n\n",
      "hellomsg": "hanks"
    })
    
    cmd( 1):
    echo "hellomsg  - {{.hellomsg}}"
    
    cmd=>:
    echo "hellomsg  - hanks"
    -
    hellomsg  - hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=24) "echo \"hellomsg  - hanks\"",
     Code: (int) 0,
     Output: (string) (len=17) "hellomsg  - hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "reg_hello - {{.reg_hello}}"
    
    cmd=>:
    echo "reg_hello - hello: hanks
    
    "
    -
    reg_hello - hello: hanks
    
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=33) "echo \"reg_hello - hello: hanks\n\n\"",
     Code: (int) 0,
     Output: (string) (len=24) "reg_hello - hello: hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3: [
    the hellomsg will be still availabe in this step
    it is removed but will be unavailabe in the next step
    ]
    {
      Name: "",
      Do: {
        "echo \"{{.hellomsg}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "reg_hello",
          Value: "{{deReg \"hellomsg\" }}\n",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "the hellomsg will be still availabe in this step\nit is removed but will be unavailabe in the next step\n",
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
        Cmd: "echo \"reg_hello - hello: hanks\n\n\"",
        Code: 0,
        Output: "reg_hello - hello: hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "reg_hello": "\n"
    }
    
    
    scope[local] merged: {
      "hellomsg": "hanks",
      "reg_hello": "\n",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"reg_hello - hello: hanks\n\n\"",
        Code: 0,
        Output: "reg_hello - hello: hanks",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"reg_hello - hello: hanks\n\n\"",
        Code: 0,
        Output: "reg_hello - hello: hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0,
      "reg_hello": "\n"
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
    cmd=>:
    echo "hanks"
    -
    hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hanks\"",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step4: [
    now the hellomsg should be <no value>
    ]
    {
      Name: "",
      Do: {
        "echo \"{{.hellomsg}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "now the hellomsg should be <no value>\n",
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
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"<no value>\"",
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        "echo '{{.iamvoid}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "hello: {{ print \"something\" |reg \"iamvoid\" }}",
          Desc: "now this var name will not be shown in local automatically\nor in global if you register it as it the reg template func\nis more like a action and return sensible value\n",
          Expand: 0,
          Flags: {
            "vvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
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
    
    [local] dvar expanded result:
    {
      "iamvoid": "something"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"<no value>\"",
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "iamvoid": "something"
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo 'something'",
     Code: (int) 0,
     Output: (string) (len=9) "something",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step6:
    {
      Name: "",
      Do: {
        "echo '{{.iamvoid}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
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
      "iamvoid": "something",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'something'",
        Code: 0,
        Output: "something",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "iamvoid": "something",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'something'",
        Code: 0,
        Output: "something",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "iamvoid": "something",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'something'",
        Code: 0,
        Output: "something",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo '{{.iamvoid}}'
    
    cmd=>:
    echo 'something'
    -
    something
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo 'something'",
     Code: (int) 0,
     Output: (string) (len=9) "something",
     ErrMsg: (string) ""
    }
    
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
