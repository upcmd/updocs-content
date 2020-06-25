---
title: "c0063_vvvv"
date: 2020-06-25T01:55:47+66:00
draft: false
weight: 10633

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
                 Verbose -> vvvv
              ModuleName -> happy_hoover8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0063
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [happy_hoover8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "global-var-a"
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
      "b": "runtime-var-b",
      "a": "global-var-a"
    })
    
    happy_hoover8: overall final exec vars:
    
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
    cmd( 2):
    echo "hello {{.a}}"
    
     \_ echo "hello global-var-a"
    hello global-var-a
     .. ok
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
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "b": "runtime-var-b"
    })
    
    happy_hoover8: overall final exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      }),
      "b": "runtime-var-b"
    })
    
    Enter Value For pause action to continue: 
    
    enter: continue 
        q: quit
        i: inspect
    
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
    
    happy_hoover8: overall final exec vars:
    
    (*core.Cache)({
      "a": "global-var-a",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello global-var-a",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "next step"
    
     \_ echo "next step"
    next step
     .. ok
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
