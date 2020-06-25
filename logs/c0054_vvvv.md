---
title: "c0054_vvvv"
date: 2020-06-25T01:55:46+66:00
draft: false
weight: 10543

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
                 Verbose -> vvvv
              ModuleName -> gloomy_mcclintock8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0054
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [gloomy_mcclintock8] instance id: [dev]
    merged[ dev ] runtime vars:
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
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello, world"
    
     \_ echo "hello, world"
    hello, world
     .. ok
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    echo "step1"
    
     \_ echo "step1"
    step1
     .. ok
    cmd( 2):
    echo "step2" |grep notexist
    
     \_ echo "step2" |grep notexist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    cmd( 3):
    echo "step3"
    
     \_ echo "step3"
    step3
     .. ok
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    cmd( 2):
    echo "{{.last_result|toJson}}"
    
     \_ echo "{"Code":0,"Output":"hello, world","ErrMsg":""}"
    {Code:0,Output:hello, world,ErrMsg:}
     .. ok
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
    cmd( 4):
    echo "{{eq .last_result.Code 0}}"
    
     \_ echo "true"
    true
     .. ok
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    cmd( 2):
    echo "step2" |grep notexist
    
     \_ echo "step2" |grep notexist
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
        "name": "peter",
        "sex": "male",
        "age": 23
      }
    })
    
    dvar> condition:
    "true"
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "condition": "true",
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    echo "simple dvar as condition"
    
     \_ echo "simple dvar as condition"
    simple dvar as condition
     .. ok
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
          "sex": "male",
          "age": 23,
          "name": "peter"
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
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "simple dvar as condition",
        ErrMsg: ""
      }),
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      },
      "condition": "true"
    })
    
    cmd( 1):
    echo "complicated dvar evaluation as condition"
    
     \_ echo "complicated dvar evaluation as condition"
    complicated dvar evaluation as condition
     .. ok
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
          "name": "peter",
          "sex": "male",
          "age": 23
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
        "name": "peter",
        "sex": "male",
        "age": 23
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      })
    })
    
    dvar> condition:
    "true"
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
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
    })
    
    cmd( 1):
    echo "a even more complicated condition but more readable"
    
     \_ echo "a even more complicated condition but more readable"
    a even more complicated condition but more readable
     .. ok
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
    
    gloomy_mcclintock8: overall final exec vars:
    
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
    
    cmd( 1):
    echo "a complicated condition without dvar"
    
     \_ echo "a complicated condition without dvar"
    a complicated condition without dvar
     .. ok
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
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
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
    
    gloomy_mcclintock8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      }),
      "doc": "hello"
    })
    
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
