---
title: "c0090_vvvvv"
date: 2020-07-01T15:34:33+77:00
draft: false
weight: 10904

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
                 Verbose -> vvvvv
              ModuleName -> compassionate_sammet9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0090
    -------full vars in scopes------
    (*impl.Scopes)(0xc000181480)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [compassionate_sammet9] instance id: [dev]
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "taskvar": "taskvar"
    }
    
    
    compassionate_sammet9: overall final exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar"
    })
    
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "loopindex1": 1,
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0
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
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "tom"
    })
    
    dvar> person:
    "tom"
    
    dvar> greet:
    "hello"
    
    [local] dvar expanded result:
    {
      "person": "tom",
      "greet": "hello"
    }
    
    
    scope[local] merged: {
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "person": "tom",
      "greet": "hello"
    }
    
    
    compassionate_sammet9: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "person": "tom",
      "greet": "hello",
      "loopitem": "tom",
      "loopindex": 0
    })
    
    callee2: {{.person}}
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: tom
    callee2: {{.loopitem}}
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: tom
    callee2: {{.greet}}
    ~~SubStep3: [print:  ]
    callee2: hello
    taskvar: {{.taskvar}}
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "loopindex1": 2,
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1
    })
    
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
    
    [local] dvar expanded result:
    {
      "person": "peter",
      "greet": "hello"
    }
    
    
    scope[local] merged: {
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2,
      "person": "peter",
      "greet": "hello",
      "up_runtime_task_layer_number": 1
    }
    
    
    compassionate_sammet9: overall final exec vars:
    
    (*core.Cache)({
      "person": "peter",
      "greet": "hello",
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    callee2: {{.person}}
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: peter
    callee2: {{.loopitem}}
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: peter
    callee2: {{.greet}}
    ~~SubStep3: [print:  ]
    callee2: hello
    taskvar: {{.taskvar}}
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3,
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
      "up_runtime_task_layer_number": 1,
      "loopindex1": 3,
      "taskvar": "taskvar",
      "loopitem": "james",
      "loopindex": 2
    })
    
    dvar> person:
    "james"
    
    dvar> greet:
    "hello"
    
    [local] dvar expanded result:
    {
      "person": "james",
      "greet": "hello"
    }
    
    
    scope[local] merged: {
      "taskvar": "taskvar",
      "loopitem": "james",
      "person": "james",
      "greet": "hello",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1,
      "loopindex1": 3
    }
    
    
    compassionate_sammet9: overall final exec vars:
    
    (*core.Cache)({
      "loopindex1": 3,
      "taskvar": "taskvar",
      "loopitem": "james",
      "person": "james",
      "greet": "hello",
      "loopindex": 2,
      "up_runtime_task_layer_number": 1
    })
    
    callee2: {{.person}}
    ~~SubStep1: [print: as explained, this should be <no value> ]
    callee2: james
    callee2: {{.loopitem}}
    ~~SubStep2: [print: this will be the loopitem from parent caller's
    var space and this is design
     ]
    callee2: james
    callee2: {{.greet}}
    ~~SubStep3: [print:  ]
    callee2: hello
    taskvar: {{.taskvar}}
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
