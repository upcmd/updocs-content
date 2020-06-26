---
title: "c0041_vvvvv"
date: 2020-06-27T03:09:19+66:00
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
              ModuleName -> mad_swartz6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0041
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb0e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [mad_swartz6] instance id: [dev]
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
    
    
    mad_swartz6: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hello
    
     \_ echo hello
    hello
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hello",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo world
    
     \_ echo world
    world
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    }
    
    
    mad_swartz6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo tom
    
     \_ echo tom
    tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result.Code}}"
    
     \_ echo "0"
    0
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=1) "0",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.last_result.Output}}"
    
     \_ echo "world"
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "world",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
      "greet": "hello: hanks\n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "greet": "hello: hanks\n"
    }
    
    
    mad_swartz6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "greet": "hello: hanks\n"
    })
    
    cmd( 1):
    echo tom
    
     \_ echo tom
    tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result.Output}}"
    
     \_ echo "hanks"
    hanks
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{.greet}}"
    
     \_ echo "hello: hanks
    "
    hello: hanks
     .. ok
    (utils.ExecResult) {
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
