---
title: "c0035_vvvvv"
date: 2020-06-27T03:09:18+66:00
draft: false
weight: 10354

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0035
                 Verbose -> vvvvv
              ModuleName -> romantic_mcclintock3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0035
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ecf20)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [romantic_mcclintock3] instance id: [dev]
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [step1:  ]
    {
      Name: "step1",
      Do: {
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "aaa",
        "b": "bbb"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "b": "bbb"
    }
    
    
    romantic_mcclintock3: overall final exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb"
    })
    
    cmd( 1):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "/up_project/up",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        "echo \"{{.a}}\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    }
    
    
    romantic_mcclintock3: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.a}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0035 log - verbose level v](../../logs/c0035_v)
* [c0035 log - verbose level vv](../../logs/c0035_vv)
* [c0035 log - verbose level vvv](../../logs/c0035_vvv)
* [c0035 log - verbose level vvvv](../../logs/c0035_vvvv)
* [c0035 log - verbose level vvvvv](../../logs/c0035_vvvvv)

##### References
* [Related Chapter](../../vars/c0035)
