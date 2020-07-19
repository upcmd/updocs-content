---
title: "c0090_vvvvv"
date: 2020-07-20T02:01:45+77:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0090
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175640)(<nil>)
    
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
    
    -Step1: [wrong_usage: note that you can't access loopitem in dvar processing in curent func
    you can only access loopitem in dvar processing when it is called as callee, as corret_usage shows
    however you can access loopitem in do action
     ]
    {
      Name: "wrong_usage",
      Do: {
        {
          "name": "print",
          "cmd": "loopitme could be accessed here: {{.loopitem}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "person",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
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
      Desc: "note that you can't access loopitem in dvar processing in curent func\nyou can only access loopitem in dvar processing when it is called as callee, as corret_usage shows\nhowever you can access loopitem in do action\n",
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
    })
    
    dvar> person:
    "None"
    
    [local] dvar expanded result:
    {
      "person": "None"
    }
    
    
    scope[local] merged: {
      "person": "None"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "None"
    })
    
    loopitme could be accessed here: {{.loopitem}}
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: tom
    
    loopitme could be accessed here: {{.loopitem}}
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: peter
    
    loopitme could be accessed here: {{.loopitem}}
    
    ~SubStep1: [print:  ]
    loopitme could be accessed here: james
    
    -Step2: [corret_usage:  ]
    {
      Name: "corret_usage",
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
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar"
    })
    
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1
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
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
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
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "taskvar": "taskvar"
    })
    
    dvar> person:
    "tom"
    
    [local] dvar expanded result:
    {
      "person": "tom"
    }
    
    
    scope[local] merged: {
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "tom",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "tom"
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
    callee2: <no value>
    taskvar: {{.taskvar}}
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2
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
          "cmd": "taskvar: {{.taskvar}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "person",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
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
    
    [local] dvar expanded result:
    {
      "person": "peter"
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "peter",
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "peter",
      "taskvar": "taskvar",
      "loopitem": "peter",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
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
    callee2: <no value>
    taskvar: {{.taskvar}}
    ~~SubStep4: [print:  ]
    taskvar: taskvar
    caller's vars to task (task_callee2)::
    (*core.Cache)({
      "taskvar": "taskvar",
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3
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
          Desc: "",
          Expand: 0,
          Flags: {
            "v"
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    dvar> person:
    "james"
    
    [local] dvar expanded result:
    {
      "person": "james"
    }
    
    
    scope[local] merged: {
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3,
      "taskvar": "taskvar",
      "up_runtime_task_layer_number": 1,
      "person": "james"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "taskvar": "taskvar",
      "up_runtime_task_layer_number": 1,
      "person": "james",
      "loopitem": "james",
      "loopindex": 2,
      "loopindex1": 3
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
    callee2: <no value>
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
