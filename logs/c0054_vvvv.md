---
title: "c0054_vvvv"
date: 2020-07-20T02:01:39+77:00
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
              ModuleName -> self
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
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
    current exec runtime vars:
    (*core.Cache)({
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"<=
    hello, world
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hello, world\"",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
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
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
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
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>)
    })
    
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
    cmd( 2):
    echo "step2" |grep notexist
    
    cmd=>:
    echo "step2" |grep notexist<=
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
    cmd( 3):
    echo "step3"
    
    cmd=>:
    echo "step3"<=
    step3
     .. ok
    . ok
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step3\"",
        Code: 0,
        Output: "step3",
        ErrMsg: ""
      })
    })
    
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
    . ok
    -Step6:
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
    cmd( 2):
    echo "{{.last_result|toJson}}"
    
    cmd=>:
    echo "{"Cmd":"echo \"hello, world\"","Code":0,"Output":"hello, world","ErrMsg":""}"<=
    {Cmd:echo "hello, world",Code:0,Output:hello, world,ErrMsg:}
     .. ok
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
    cmd( 4):
    echo "{{eq .last_result.Code 0}}"
    
    cmd=>:
    echo "true"<=
    true
     .. ok
    . ok
    -Step7:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"true\"",
        Code: 0,
        Output: "true",
        ErrMsg: ""
      })
    })
    
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
    cmd( 2):
    echo "step2" |grep notexist
    
    cmd=>:
    echo "step2" |grep notexist<=
          exec error: -> exit status 1
    -----trace for reference-----
    
          
     .. failed(suppressed if not last step)
     WARN: [HightLight:] - [Error ignored!!!]
    -Step8:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step2\" |grep notexist",
        Code: 1,
        Output: "",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"step2\" |grep notexist",
        Code: 1,
        Output: "",
        ErrMsg: ""
      })
    })
    
    condition failed, skip executing step 
    
    -Step9:
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
    
    self: final context exec vars:
    
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
    
    cmd=>:
    echo "simple dvar as condition"<=
    simple dvar as condition
     .. ok
    . ok
    -Step10:
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
    
    self: final context exec vars:
    
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
      },
      "condition": "true"
    })
    
    cmd( 1):
    echo "complicated dvar evaluation as condition"
    
    cmd=>:
    echo "complicated dvar evaluation as condition"<=
    complicated dvar evaluation as condition
     .. ok
    . ok
    -Step11:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"complicated dvar evaluation as condition\"",
        Code: 0,
        Output: "complicated dvar evaluation as condition",
        ErrMsg: ""
      }),
      "student": {
        "age": 23,
        "name": "peter",
        "sex": "male"
      }
    })
    
    dvar> condition:
    "true"
    
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
    . ok
    -Step12:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "sex": "male",
        "age": 23,
        "name": "peter"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a even more complicated condition but more readable\"",
        Code: 0,
        Output: "a even more complicated condition but more readable",
        ErrMsg: ""
      })
    })
    
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
    . ok
    -Step13: [: show that complicated arg needs to be quoted using ()
    otherwise it will cause gt to be confused
     ]
    current exec runtime vars:
    (*core.Cache)({
      "doc": "hello",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"a complicated condition without dvar\"",
        Code: 0,
        Output: "a complicated condition without dvar",
        ErrMsg: ""
      })
    })
    
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
    
    ~SubStep1: [print:  ]
    true
    -Step14:
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
