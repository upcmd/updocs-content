---
title: "c0041_vvvv"
date: 2020-06-25T01:55:43+66:00
draft: false
weight: 10413

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
                 Verbose -> vvvv
              ModuleName -> hungry_bartik8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0041
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hungry_bartik8] instance id: [dev]
    merged[ dev ] runtime vars:
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
    
    hungry_bartik8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo hello
    
     \_ echo hello
    hello
     .. ok
    cmd( 2):
    echo world
    
     \_ echo world
    world
     .. ok
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
    
    hungry_bartik8: overall final exec vars:
    
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
    cmd( 2):
    echo "{{.last_result.Code}}"
    
     \_ echo "0"
    0
     .. ok
    cmd( 3):
    echo "{{.last_result.Output}}"
    
     \_ echo "world"
    world
     .. ok
    cmd( 4):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
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
    
    hungry_bartik8: overall final exec vars:
    
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
    cmd( 2):
    echo "{{.last_result.Output}}"
    
     \_ echo "hanks"
    hanks
     .. ok
    cmd( 3):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    cmd( 4):
    echo "{{.greet}}"
    
     \_ echo "hello: hanks
    "
    hello: hanks
     .. ok
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
