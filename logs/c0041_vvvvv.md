---
title: "c0041_vvvvv"
date: 2020-09-18T01:27:27+99:00
draft: false
weight: 10414

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0041
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
    loading [Task]:  ./tests/functests/c0041
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e5120)(<nil>)
    
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
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    {
      Name: "",
      Do: {
        "echo hello",
        "echo world"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step1",
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
    echo hello
    
    cmd=>:
    echo hello
    -
    hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hello",
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo world
    
    cmd=>:
    echo world
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo world",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: step2 ]
    {
      Name: "",
      Do: {
        "echo tom",
        "echo \"{{.last_result.Code}}\"",
        "echo \"{{.last_result.Output}}\"",
        "echo hanks"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step2",
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
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo world",
        Code: 0,
        Output: "world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo tom
    
    cmd=>:
    echo tom
    -
    tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "echo tom",
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result.Code}}"
    
    cmd=>:
    echo "0"
    -
    0
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "echo \"0\"",
     Code: (int) 0,
     Output: (string) (len=1) "0",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.last_result.Output}}"
    
    cmd=>:
    echo "world"
    -
    world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"world\"",
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo hanks
    
    cmd=>:
    echo hanks
    -
    hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hanks",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3: [: step3 ]
    {
      Name: "",
      Do: {
        "echo tom",
        "echo \"{{.last_result.Output}}\"",
        "echo hanks",
        "echo \"{{.greet}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "greet",
          Value: "hello: {{.last_result.Output}}\n",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "step3",
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
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "greet": "hello: hanks\n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "greet": "hello: hanks\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "greet": "hello: hanks\n"
    })
    
    cmd( 1):
    echo tom
    
    cmd=>:
    echo tom
    -
    tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=8) "echo tom",
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result.Output}}"
    
    cmd=>:
    echo "hanks"
    -
    hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"hanks\"",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo hanks
    
    cmd=>:
    echo hanks
    -
    hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo hanks",
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{.greet}}"
    
    cmd=>:
    echo "hello: hanks
    "
    -
    hello: hanks
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"hello: hanks\n\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello: hanks",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0041 log - verbose level v](../../logs/c0041_v)
* [c0041 log - verbose level vv](../../logs/c0041_vv)
* [c0041 log - verbose level vvv](../../logs/c0041_vvv)
* [c0041 log - verbose level vvvv](../../logs/c0041_vvvv)
* [c0041 log - verbose level vvvvv](../../logs/c0041_vvvvv)

##### References
* [Related Chapter](../../shell-func/c0041)
