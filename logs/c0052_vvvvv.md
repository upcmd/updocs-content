---
title: "c0052_vvvvv"
date: 2020-06-25T01:55:45+66:00
draft: false
weight: 10524

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0052
                 Verbose -> vvvvv
              ModuleName -> determined_hodgkin0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0052
    -------full vars in scopes------
    (*impl.Scopes)(0xc000187120)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_hodgkin0] instance id: [dev]
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
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"step1\"",
        "echo \"step2\" |grep notexist",
        "echo \"step3\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignore_error"
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
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    determined_hodgkin0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "step1"
    
     \_ echo "step1"
    step1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step2" |grep notexist
    
     \_ echo "step2" |grep notexist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    (utils.ExecResult) {
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step3"
    
     \_ echo "step3"
    step3
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step3",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"step4\"",
        "echo \"step5\" |grep notexist",
        "echo \"step6\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignore_error"
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
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    }
    
    
    determined_hodgkin0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "step4"
    
     \_ echo "step4"
    step4
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step4",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step5" |grep notexist
    
     \_ echo "step5" |grep notexist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    (utils.ExecResult) {
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step6"
    
     \_ echo "step6"
    step6
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step6",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"step7\"",
        "echo \"step8\"",
        "echo \"step9\""
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
        Output: "step6",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      })
    }
    
    
    determined_hodgkin0: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "step7"
    
     \_ echo "step7"
    step7
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step7",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step8"
    
     \_ echo "step8"
    step8
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step8",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step9"
    
     \_ echo "step9"
    step9
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "step9",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0052 log - verbose level v](../../logs/c0052_v)
* [c0052 log - verbose level vv](../../logs/c0052_vv)
* [c0052 log - verbose level vvv](../../logs/c0052_vvv)
* [c0052 log - verbose level vvvv](../../logs/c0052_vvvv)
* [c0052 log - verbose level vvvvv](../../logs/c0052_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0052)
