---
title: "c0059_vvvvv"
date: 2020-10-07T00:11:10+1010:00
draft: false
weight: 10594

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
    loading [Task]:  ./tests/functests/c0059
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c0e60)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e8d0)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
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
    echo "step1"
    
    cmd=>:
    echo "step1"
    -
    step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step1\"",
     Code: (int) 0,
     Output: (string) (len=5) "step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step2"
    
    cmd=>:
    echo "step2"
    -
    step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step2\"",
     Code: (int) 0,
     Output: (string) (len=5) "step2",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step3"
    
    cmd=>:
    echo "step3"
    -
    step3
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step3\"",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
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
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "step4"
    
    cmd=>:
    echo "step4"
    -
    step4
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step4\"",
     Code: (int) 0,
     Output: (string) (len=5) "step4",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step5"
    
    cmd=>:
    echo "step5"
    -
    step5
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step5\"",
     Code: (int) 0,
     Output: (string) (len=5) "step5",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step6"
    
    cmd=>:
    echo "step6"
    -
    step6
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step6\"",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "step7"
    
    cmd=>:
    echo "step7"
    -
    step7
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step7\"",
     Code: (int) 0,
     Output: (string) (len=5) "step7",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "step8"
    
    cmd=>:
    echo "step8"
    -
    step8
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step8\"",
     Code: (int) 0,
     Output: (string) (len=5) "step8",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "step9"
    
    cmd=>:
    echo "step9"
    -
    step9
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step9\"",
     Code: (int) 0,
     Output: (string) (len=5) "step9",
     ErrMsg: (string) ""
    }
    
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
