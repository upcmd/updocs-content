---
title: "c0054_vvvvv"
date: 2020-07-01T15:34:28+77:00
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
              ModuleName -> fervent_jang6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0054
    -------full vars in scopes------
    (*impl.Scopes)(0xc000231300)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [fervent_jang6] instance id: [dev]
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
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello, world"
    
     \_ echo "hello, world"
    hello, world
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
      VarsFile: ""
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
    
    
    fervent_jang6: overall final exec vars:
    
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
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)(<nil>)
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
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
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "hello, world"
    
     \_ echo "hello, world"
    hello, world
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    dvar> last_task_succeeded:
    "true"
    
    [local] dvar expanded result:
    {
      "last_task_succeeded": "true"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "last_task_succeeded": "true"
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "last_task_succeeded": "true"
    })
    
    cmd( 1):
    echo "check last step"
    
     \_ echo "check last step"
    check last step
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=15) "check last step",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.last_result|toJson}}"
    
     \_ echo "{"Code":0,"Output":"hello, world","ErrMsg":""}"
    {Code:0,Output:hello, world,ErrMsg:}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=36) "{Code:0,Output:hello, world,ErrMsg:}",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.last_result|toPrettyJson}}"
    
     \_ echo "{
      "Code": 0,
      "Output": "hello, world",
      "ErrMsg": ""
    }"
    {
      Code: 0,
      Output: hello, world,
      ErrMsg: 
    }
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=49) "{\n  Code: 0,\n  Output: hello, world,\n  ErrMsg: \n}",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{eq .last_result.Code 0}}"
    
     \_ echo "true"
    true
     .. ok
    (utils.ExecResult) {
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
        Output: "true",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 1,
        Output: "",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 1,
        Output: "",
        ErrMsg: ""
      })
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 1,
        Output: "",
        ErrMsg: ""
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
      VarsFile: ""
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
    
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "condition": "true",
      "last_result": (*utils.ExecResult)(<nil>)
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>),
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      },
      "condition": "true"
    })
    
    cmd( 1):
    echo "simple dvar as condition"
    
     \_ echo "simple dvar as condition"
    simple dvar as condition
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
    
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
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
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
    })
    
    cmd( 1):
    echo "complicated dvar evaluation as condition"
    
     \_ echo "complicated dvar evaluation as condition"
    complicated dvar evaluation as condition
     .. ok
    (utils.ExecResult) {
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
          "sex": "male",
          "age": 23,
          "name": "peter"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      })
    })
    
    dvar> condition:
    "true"
    
    [local] dvar expanded result:
    {
      "condition": "true"
    }
    
    
    scope[local] merged: {
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      }),
      "condition": "true"
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "condition": "true",
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "a even more complicated condition but more readable"
    
     \_ echo "a even more complicated condition but more readable"
    a even more complicated condition but more readable
     .. ok
    (utils.ExecResult) {
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
          "name": "peter",
          "sex": "male",
          "age": 23
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      }),
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      }
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      }),
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      }
    })
    
    cmd( 1):
    echo "a complicated condition without dvar"
    
     \_ echo "a complicated condition without dvar"
    a complicated condition without dvar
     .. ok
    (utils.ExecResult) {
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
      "doc": "hello",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      })
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "doc": "hello",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      })
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    }
    
    
    fervent_jang6: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
