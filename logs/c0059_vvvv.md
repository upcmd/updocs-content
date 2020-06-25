---
title: "c0059_vvvv"
date: 2020-06-25T01:55:46+66:00
draft: false
weight: 10593

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0059
                 Verbose -> vvvv
              ModuleName -> compassionate_poincare2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0059
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [compassionate_poincare2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    loading [flow ref]:  ./tests/functests/c0059-task-ref.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"step1\"",
        "echo \"step2\"",
        "echo \"step3\""
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
    })
    
    compassionate_poincare2: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "step1"
    
     \_ echo "step1"
    step1
     .. ok
    cmd( 2):
    echo "step2"
    
     \_ echo "step2"
    step2
     .. ok
    cmd( 3):
    echo "step3"
    
     \_ echo "step3"
    step3
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"step4\"",
        "echo \"step5\"",
        "echo \"step6\""
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
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    compassionate_poincare2: overall final exec vars:
    
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
    cmd( 2):
    echo "step5"
    
     \_ echo "step5"
    step5
     .. ok
    cmd( 3):
    echo "step6"
    
     \_ echo "step6"
    step6
     .. ok
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
    
    compassionate_poincare2: overall final exec vars:
    
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
    cmd( 2):
    echo "step8"
    
     \_ echo "step8"
    step8
     .. ok
    cmd( 3):
    echo "step9"
    
     \_ echo "step9"
    step9
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0059 log - verbose level v](../../logs/c0059_v)
* [c0059 log - verbose level vv](../../logs/c0059_vv)
* [c0059 log - verbose level vvv](../../logs/c0059_vvv)
* [c0059 log - verbose level vvvv](../../logs/c0059_vvvv)
* [c0059 log - verbose level vvvvv](../../logs/c0059_vvvvv)

##### References
* [Related Chapter](../../organization/c0059)
