---
title: "c0052_vvvvv"
date: 2020-09-18T00:51:27+99:00
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
    loading [Task]:  ./tests/functests/c0052
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e71a0)(<nil>)
    
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
        "ignoreError"
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
    echo "step2" |grep notexist
    
    cmd=>:
    echo "step2" |grep notexist
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"step2\" |grep notexist",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
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
        "ignoreError"
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
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
    echo "step5" |grep notexist
    
    cmd=>:
    echo "step5" |grep notexist
    -
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"step5\" |grep notexist",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
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
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step6\"",
        Code: 0,
        Output: "step6",
        ErrMsg: ""
      })
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
* [c0052 log - verbose level v](../../logs/c0052_v)
* [c0052 log - verbose level vv](../../logs/c0052_vv)
* [c0052 log - verbose level vvv](../../logs/c0052_vvv)
* [c0052 log - verbose level vvvv](../../logs/c0052_vvvv)
* [c0052 log - verbose level vvvvv](../../logs/c0052_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0052)
