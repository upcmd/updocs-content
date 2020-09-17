---
title: "0002_vvvvv"
date: 2020-09-18T00:52:27+99:00
draft: false
weight: 100204

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0002/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0002
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0002
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> Main
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0002
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001730a0)(<nil>)
    
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
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: main job ]
    {
      Name: "",
      Do: {
        "echo \"hello world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "main job",
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
    echo "hello world"
    
    cmd=>:
    echo "hello world"
    -
    hello world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"hello world\"",
     Code: (int) 0,
     Output: (string) (len=11) "hello world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: "internal_task",
      Dox: <nil>,
      Func: "call",
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (internal_task)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [internal_task]: 
    =Task2: [Main ==> internal_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "this is a internal task"
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    this is a internal task
    ~~SubStep1: [print:  ]
    this is a internal task
    -Step3:
    {
      Name: "",
      Do: "hello-module.Say_world",
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "caller-aaa"
      },
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
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    })
    
    caller's vars to task (hello-module.Say_world)::
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "a": "caller-aaa"
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed980)(<nil>)
    
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
    
    =>call module: [hello-module] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "... module world\na: {{.a}}\nb: {{.b}}\n"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"caller-aaa\"}}",
            "{{eq .b \"module-bbb\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "module-aaa",
        "b": "module-bbb"
      },
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
      "a": "caller-aaa",
      "b": "module-bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-aaa",
      "b": "module-bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-aaa",
      "b": "module-bbb",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello world\"",
        Code: 0,
        Output: "hello world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    ... module world
    a: {{.a}}
    b: {{.b}}
    
    ~SubStep1: [print:  ]
    ... module world
    a: caller-aaa
    b: module-bbb
    
    [{{eq .a "caller-aaa"}} {{eq .b "module-bbb"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "caller-aaa"}}]
     2 ASSERT OK:     [{{eq .b "module-bbb"}}]
    
```

##### Logs with different verbose level
* [m0002 log - verbose level v](../../logs/m0002_v)
* [m0002 log - verbose level vv](../../logs/m0002_vv)
* [m0002 log - verbose level vvv](../../logs/m0002_vvv)
* [m0002 log - verbose level vvvv](../../logs/m0002_vvvv)
* [m0002 log - verbose level vvvvv](../../logs/m0002_vvvvv)

##### References
* [Related Chapter](../../module/0002)
