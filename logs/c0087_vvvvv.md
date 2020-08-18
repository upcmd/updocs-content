---
title: "c0087_vvvvv"
date: 2020-08-18T15:16:04+88:00
draft: false
weight: 10874

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0087
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0087
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c15c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo 'hello'"
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
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo 'hello'
    
    cmd=>:
    echo 'hello'
    -
    hello
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo 'hello'",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "cmd": 2000
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    %!s(int=2000)
    ~SubStep1: [sleep:  ]
    sleeping 2000 milli seconds
    ....................
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "world"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    world
    ~SubStep1: [print:  ]
    world
    -Step4:
    {
      Name: "",
      Do: {
        "{{.loopitem}}"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "impl1",
        "impl2"
      },
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
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (impl1)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [impl1]: 
    =Task2: [task ==> impl1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1"
    })
    
    hello
    ~~SubStep1: [print:  ]
    hello
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "sleep",
          "cmd": 1000
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "loopindex": 0,
      "up_runtime_task_layer_number": 1,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl1",
      "loopindex": 0,
      "up_runtime_task_layer_number": 1
    })
    
    %!s(int=1000)
    ~~SubStep1: [sleep:  ]
    sleeping 1000 milli seconds
    ..........
    caller's vars to task (impl2)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [impl2]: 
    =Task3: [task ==> impl2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "world"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo 'hello'",
        Code: 0,
        Output: "hello",
        ErrMsg: ""
      }),
      "loopitem": "impl2"
    })
    
    world
    ~~SubStep1: [print:  ]
    world
    
```

##### Logs with different verbose level
* [c0087 log - verbose level v](../../logs/c0087_v)
* [c0087 log - verbose level vv](../../logs/c0087_vv)
* [c0087 log - verbose level vvv](../../logs/c0087_vvv)
* [c0087 log - verbose level vvvv](../../logs/c0087_vvvv)
* [c0087 log - verbose level vvvvv](../../logs/c0087_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0087)
