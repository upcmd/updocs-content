---
title: "c0090_vvvv"
date: 2020-06-27T03:09:26+66:00
draft: false
weight: 10903

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0090
                 Verbose -> vvvv
              ModuleName -> jolly_blackwell5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0090
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [jolly_blackwell5] instance id: [dev]
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
        "task_callee2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "taskvar": "taskvar"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "tom",
        "peter",
        "james"
      },
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "taskvar": "taskvar"
    })
    
    jolly_blackwell5: overall final exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar"
    })
    
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "as explained, this should be <no value>",
          "cmd": "callee2: {{.person}}"
        },
        {
          "cmd": "callee2: {{.loopitem}}",
          "name": "print",
          "desc": "this will be the loopitem from parent caller's\nvar space and this is design\n"
        },
        {
          "name": "print",
          "cmd": "callee2: {{.greet}}"
        },
        {
          "name": "print",
          "cmd": "taskvar: {{.taskvar}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "person",
          Value: "{{.loopitem}}",
          Desc: "loopitem is not availab yet when dvar is expanded\ndue to the design that caller's var will override\nthe callee's var, the loopitem should not be availabe\nin dvar and this is not a bug\n",
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
        },
        {
          Name: "greet",
          Value: "hello",
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
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    dvar> person:
    "tom"
    
    dvar> greet:
    "hello"
    
    jolly_blackwell5: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "tom",
      "person": "tom",
      "greet": "hello",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar"
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: tom
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: tom
    ~~SubStep3: [print:  ]
    callee2: hello
    ~~SubStep4: [print:  ]
    taskvar: taskvar
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "as explained, this should be <no value>",
          "cmd": "callee2: {{.person}}"
        },
        {
          "cmd": "callee2: {{.loopitem}}",
          "name": "print",
          "desc": "this will be the loopitem from parent caller's\nvar space and this is design\n"
        },
        {
          "name": "print",
          "cmd": "callee2: {{.greet}}"
        },
        {
          "name": "print",
          "cmd": "taskvar: {{.taskvar}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "person",
          Value: "{{.loopitem}}",
          Desc: "loopitem is not availab yet when dvar is expanded\ndue to the design that caller's var will override\nthe callee's var, the loopitem should not be availabe\nin dvar and this is not a bug\n",
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
        },
        {
          Name: "greet",
          Value: "hello",
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
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    dvar> person:
    "peter"
    
    dvar> greet:
    "hello"
    
    jolly_blackwell5: overall final exec vars:
    
    (*core.Cache)({
      "person": "peter",
      "greet": "hello",
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: peter
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: peter
    ~~SubStep3: [print:  ]
    callee2: hello
    ~~SubStep4: [print:  ]
    taskvar: taskvar
      located task-> 3 [task_callee2]: 
    =Task3: [task ==> task_callee2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "callee2: {{.person}}",
          "name": "print",
          "desc": "as explained, this should be <no value>"
        },
        {
          "name": "print",
          "desc": "this will be the loopitem from parent caller's\nvar space and this is design\n",
          "cmd": "callee2: {{.loopitem}}"
        },
        {
          "name": "print",
          "cmd": "callee2: {{.greet}}"
        },
        {
          "name": "print",
          "cmd": "taskvar: {{.taskvar}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "person",
          Value: "{{.loopitem}}",
          Desc: "loopitem is not availab yet when dvar is expanded\ndue to the design that caller's var will override\nthe callee's var, the loopitem should not be availabe\nin dvar and this is not a bug\n",
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
        },
        {
          Name: "greet",
          Value: "hello",
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
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 3,
      "taskvar": "taskvar",
      "loopitem": "james",
      "up_runtime_task_layer_number": 1,
      "loopindex": 2
    })
    
    dvar> person:
    "james"
    
    dvar> greet:
    "hello"
    
    jolly_blackwell5: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "greet": "hello",
      "person": "james",
      "loopindex": 2,
      "loopindex1": 3,
      "taskvar": "taskvar",
      "loopitem": "james"
    })
    
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: james
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: james
    ~~SubStep3: [print:  ]
    callee2: hello
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    
```

##### Logs with different verbose level
* [c0090 log - verbose level v](../../logs/c0090_v)
* [c0090 log - verbose level vv](../../logs/c0090_vv)
* [c0090 log - verbose level vvv](../../logs/c0090_vvv)
* [c0090 log - verbose level vvvv](../../logs/c0090_vvvv)
* [c0090 log - verbose level vvvvv](../../logs/c0090_vvvvv)

##### References
* [Related Chapter](../../loop/c0090)
