---
title: "c0063_vvvvv"
date: 2020-09-18T00:51:29+99:00
draft: false
weight: 10634

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0063
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0063
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000c080)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "a": "global-var-a"
    }
    
    (core.Cache) (len=1) {
     (string) (len=1) "a": (string) (len=12) "global-var-a"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "global-var-a"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"hello\"",
        "echo \"hello {{.a}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "b": "runtime-var-b"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "pause"
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
      "a": "global-var-a",
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "global-var-a",
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    })
    
    Enter Value For [pause action to continue]: 
    
    enter: continue 
        q: quit
        i: inspect
    
    cmd( 1):
    echo "hello"
    
    cmd=>:
    echo "hello"
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hello\"",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.a}}"
    
    cmd=>:
    echo "hello global-var-a"
    -
    hello global-var-a
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"hello global-var-a\"",
     Code: (int) 0,
     Output: (string) (len=18) "hello global-var-a",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello {{.a}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "b": "runtime-var-b"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "pause"
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
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b",
      "a": "global-var-a"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "runtime-var-b",
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      })
    })
    
    Enter Value For [pause action to continue]: 
    
    enter: continue 
        q: quit
        i: inspect
    
    hello {{.a}}
    ~SubStep1: [print:  ]
    hello global-var-a
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"next step\""
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
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello global-var-a\"",
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "next step"
    
    cmd=>:
    echo "next step"
    -
    next step
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"next step\"",
     Code: (int) 0,
     Output: (string) (len=9) "next step",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0063 log - verbose level v](../../logs/c0063_v)
* [c0063 log - verbose level vv](../../logs/c0063_vv)
* [c0063 log - verbose level vvv](../../logs/c0063_vvv)
* [c0063 log - verbose level vvvv](../../logs/c0063_vvvv)
* [c0063 log - verbose level vvvvv](../../logs/c0063_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0063)
