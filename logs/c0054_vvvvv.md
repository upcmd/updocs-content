---
title: "c0054_vvvvv"
date: 2020-08-09T01:36:06+88:00
draft: false
weight: 10544

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0054
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0054
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7f00)(<nil>)
    
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
        "echo \"hello, world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "true",
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
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
    hello, world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"hello, world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "false",
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
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    condition failed, skip executing step 
    
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"hello, world\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "FALSE",
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
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    condition failed, skip executing step 
    
    -Step4: [: note that for one step, there will be only one
    return, which will be the last do cmd
    in this case, since the step3 exit code is 0
    the whole step will have the return code of 0
    if you need to use the exit code of the step
    you need to consider to reduce the number of do cmds
    or put it to last step, this is not a bug
    this is a feature
     ]
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
      Desc: "note that for one step, there will be only one\nreturn, which will be the last do cmd\nin this case, since the step3 exit code is 0\nthe whole step will have the return code of 0\nif you need to use the exit code of the step\nyou need to consider to reduce the number of do cmds\nor put it to last step, this is not a bug\nthis is a feature\n",
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
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    echo "step1"
    
    cmd=>:
    echo "step1"<=
    step1
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
    echo "step2" |grep notexist<=
          exec wait -> exit status 1
    -----trace for reference-----
          exit status 1
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
    echo "step3"<=
    step3
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=12) "echo \"step3\"",
     Code: (int) 0,
     Output: (string) (len=5) "step3",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        "echo \"hello, world\""
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
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
    hello, world
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step6:
    {
      Name: "",
      Do: {
        "echo \"check last step\"",
        "echo \"{{.last_result|toJson}}\"",
        "echo \"{{.last_result|toPrettyJson}}\"",
        "echo \"{{eq .last_result.Code 0}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "last_task_succeeded",
          Value: "{{eq .last_result.Code 0}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .last_result.Code 0}}",
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
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    dvar> last_task_succeeded:
    "true"
    
    -
    true
    [local] dvar expanded result:
    {
      "last_task_succeeded": "true"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "last_task_succeeded": "true"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "last_task_succeeded": "true"
    })
    
    cmd( 1):
    echo "check last step"
    
    cmd=>:
    echo "check last step"<=
    check last step
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"check last step\"",
     Code: (int) 0,
     Output: (string) (len=15) "check last step",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result|toJson}}"
    
    cmd=>:
    echo "{"Cmd":"echo \"hello, world\"","Code":0,"Output":"hello, world","ErrMsg":""}"<=
    {Cmd:echo "hello, world",Code:0,Output:hello, world,ErrMsg:}
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=83) "echo \"{\"Cmd\":\"echo \\\"hello, world\\\"\",\"Code\":0,\"Output\":\"hello, world\",\"ErrMsg\":\"\"}\"",
     Code: (int) 0,
     Output: (string) (len=60) "{Cmd:echo \"hello, world\",Code:0,Output:hello, world,ErrMsg:}",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.last_result|toPrettyJson}}"
    
    cmd=>:
    echo "{
      "Cmd": "echo \"hello, world\"",
      "Code": 0,
      "Output": "hello, world",
      "ErrMsg": ""
    }"<=
    {
      Cmd: echo "hello, world",
      Code: 0,
      Output: hello, world,
      ErrMsg: 
    }
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=100) "echo \"{\n  \"Cmd\": \"echo \\\"hello, world\\\"\",\n  \"Code\": 0,\n  \"Output\": \"hello, world\",\n  \"ErrMsg\": \"\"\n}\"",
     Code: (int) 0,
     Output: (string) (len=77) "{\n  Cmd: echo \"hello, world\",\n  Code: 0,\n  Output: hello, world,\n  ErrMsg: \n}",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{eq .last_result.Code 0}}"
    
    cmd=>:
    echo "true"<=
    true
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "echo \"true\"",
     Code: (int) 0,
     Output: (string) (len=4) "true",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step7:
    {
      Name: "",
      Do: {
        "echo \"step1\"",
        "echo \"step2\" |grep notexist"
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
        Cmd: "echo \"true\"",
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"true\"",
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"true\"",
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "step1"
    
    cmd=>:
    echo "step1"<=
    step1
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
    echo "step2" |grep notexist<=
          exec wait -> exit status 1
    -----trace for reference-----
          exit status 1
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"step2\" |grep notexist",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=13) "exit status 1"
    }
    
     WARN: [HightLight:] - [Error ignored!!!]
    -Step8:
    {
      Name: "",
      Do: {
        "echo \"check last step\"",
        "echo \"{{.last_result|toJson}}\"",
        "echo \"{{.last_result|toPrettyJson}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .last_result.Code 0}}",
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
        Cmd: "echo \"step2\" |grep notexist",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step2\" |grep notexist",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step2\" |grep notexist",
        Code: 1,
        Output: "",
        ErrMsg: "exit status 1"
      })
    })
    
    condition failed, skip executing step 
    
    -Step9:
    {
      Name: "",
      Do: {
        "echo \"simple dvar as condition\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": {
          "name": "peter",
          "sex": "male",
          "age": 23
        }
      },
      Dvars: {
        {
          Name: "condition",
          Value: "{{eq .student.sex \"male\"}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.condition}}",
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
      "last_result": (*utils.ExecResult)(<nil>),
      "student": {
        "sex": "male",
        "age": 23,
        "name": "peter"
      }
    })
    
    dvar> condition:
    "true"
    
    -
    true
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "condition": "true",
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "last_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "condition": "true"
    })
    
    cmd( 1):
    echo "simple dvar as condition"
    
    cmd=>:
    echo "simple dvar as condition"<=
    simple dvar as condition
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=31) "echo \"simple dvar as condition\"",
     Code: (int) 0,
     Output: (string) (len=24) "simple dvar as condition",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step10:
    {
      Name: "",
      Do: {
        "echo \"complicated dvar evaluation as condition\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": {
          "name": "peter",
          "sex": "male",
          "age": 23
        }
      },
      Dvars: {
        {
          Name: "condition",
          Value: "{{and (ge .student.age 18) (eq .student.sex \"male\") }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.condition}}",
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
        Cmd: "echo \"simple dvar as condition\"",
        Code: 0,
        Output: "simple dvar as condition",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      }
    })
    
    dvar> condition:
    "true"
    
    -
    true
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"simple dvar as condition\"",
        Code: 0,
        Output: "simple dvar as condition",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "condition": "true"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "condition": "true",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"simple dvar as condition\"",
        Code: 0,
        Output: "simple dvar as condition",
        ErrMsg: ""
      }),
      "student": {
        "sex": "male",
        "age": 23,
        "name": "peter"
      }
    })
    
    cmd( 1):
    echo "complicated dvar evaluation as condition"
    
    cmd=>:
    echo "complicated dvar evaluation as condition"<=
    complicated dvar evaluation as condition
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=47) "echo \"complicated dvar evaluation as condition\"",
     Code: (int) 0,
     Output: (string) (len=40) "complicated dvar evaluation as condition",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step11:
    {
      Name: "",
      Do: {
        "echo \"a even more complicated condition but more readable\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": {
          "age": 23,
          "name": "peter",
          "sex": "male"
        }
      },
      Dvars: {
        {
          Name: "condition",
          Value: "{{- with .student -}}\n{{and (ge .age 18) (eq .sex \"male\") }}\n{{- end -}}\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{.condition}}",
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
        Cmd: "echo \"complicated dvar evaluation as condition\"",
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      }),
      "student": {
        "sex": "male",
        "age": 23,
        "name": "peter"
      }
    })
    
    dvar> condition:
    "true"
    
    -
    true
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"complicated dvar evaluation as condition\"",
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      }),
      "student": {
        "sex": "male",
        "age": 23,
        "name": "peter"
      },
      "condition": "true"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"complicated dvar evaluation as condition\"",
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "condition": "true"
    })
    
    cmd( 1):
    echo "a even more complicated condition but more readable"
    
    cmd=>:
    echo "a even more complicated condition but more readable"<=
    a even more complicated condition but more readable
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=58) "echo \"a even more complicated condition but more readable\"",
     Code: (int) 0,
     Output: (string) (len=51) "a even more complicated condition but more readable",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step12:
    {
      Name: "",
      Do: {
        "echo \"a complicated condition without dvar\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "student": {
          "sex": "male",
          "age": 23,
          "name": "peter"
        }
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{- with .student -}}\n{{and (ge .age 18) (eq .sex \"male\") }}\n{{- end -}}\n",
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
        Cmd: "echo \"a even more complicated condition but more readable\"",
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a even more complicated condition but more readable\"",
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a even more complicated condition but more readable\"",
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      }),
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      }
    })
    
    cmd( 1):
    echo "a complicated condition without dvar"
    
    cmd=>:
    echo "a complicated condition without dvar"<=
    a complicated condition without dvar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=43) "echo \"a complicated condition without dvar\"",
     Code: (int) 0,
     Output: (string) (len=36) "a complicated condition without dvar",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step13: [: show that complicated arg needs to be quoted using ()
    otherwise it will cause gt to be confused
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{ gt (.doc|len) 1 }}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "doc": "hello"
      },
      Dvars: <nil>,
      Desc: "show that complicated arg needs to be quoted using ()\notherwise it will cause gt to be confused\n",
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
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
    {{ gt (.doc|len) 1 }}
    ~SubStep1: [print:  ]
    true
    -Step14:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{ gt (.doc|len) 1 }}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "doc": "hello"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{gt (.doc|len) 0}}",
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
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
    {{ gt (.doc|len) 1 }}
    ~SubStep1: [print:  ]
    true
    
```

##### Logs with different verbose level
* [c0054 log - verbose level v](../../logs/c0054_v)
* [c0054 log - verbose level vv](../../logs/c0054_vv)
* [c0054 log - verbose level vvv](../../logs/c0054_vvv)
* [c0054 log - verbose level vvvv](../../logs/c0054_vvvv)
* [c0054 log - verbose level vvvvv](../../logs/c0054_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0054)
