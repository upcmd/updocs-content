---
title: "c0063_vvvvv"
date: 2020-07-01T15:34:29+77:00
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
              ModuleName -> drunk_mcclintock0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0063
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed100)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [drunk_mcclintock0] instance id: [dev]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "global-var-a",
      "b": "runtime-var-b"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "global-var-a",
      "b": "runtime-var-b"
    }
    
    
    drunk_mcclintock0: overall final exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "b": "runtime-var-b"
    })
    
    Enter Value For pause action to continue: 
    
    enter: continue 
        q: quit
        i: inspect
    
    cmd( 1):
    echo "hello"
    
     \_ echo "hello"
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "hello {{.a}}"
    
     \_ echo "hello global-var-a"
    hello global-var-a
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "b": "runtime-var-b",
      "a": "global-var-a"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "b": "runtime-var-b",
      "a": "global-var-a"
    }
    
    
    drunk_mcclintock0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "b": "runtime-var-b",
      "a": "global-var-a"
    })
    
    Enter Value For pause action to continue: 
    
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "a": "global-var-a"
    }
    
    
    drunk_mcclintock0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "a": "global-var-a"
    })
    
    cmd( 1):
    echo "next step"
    
     \_ echo "next step"
    next step
     .. ok
    (utils.ExecResult) {
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
