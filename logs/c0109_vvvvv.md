---
title: "c0109_vvvvv"
date: 2020-07-01T15:34:36+77:00
draft: false
weight: 11094

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0109
                 Verbose -> vvvvv
              ModuleName -> reverent_darwin4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0109
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed440)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [reverent_darwin4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom"
    }
    
    (core.Cache) (len=1) {
     (string) (len=3) "tom": (string) (len=11) "this is tom"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "desc": "this should print out the dvar value of jerry",
          "cmd": "{{.jerry}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "jerry",
          Value: "this is jerry in task scope",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskscope"
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
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
      "jerry": "this is jerry in task scope"
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    }
    
    
    reverent_darwin4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "this is tom",
      "jerry": "this is jerry in task scope"
    })
    
    {{.jerry}}
    ~SubStep1: [print: this should print out the dvar value of jerry ]
    this is jerry in task scope
    -Step2:
    {
      Name: "",
      Do: {
        "subtask1"
      },
      Dox: <nil>,
      Func: "call",
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
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    }
    
    
    reverent_darwin4: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the dvar value of jerry as it is declared jerry is in taskscope",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "===>"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    }
    
    
    reverent_darwin4: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    {{.jerry}}
    ~~SubStep1: [print: this should print out the dvar value of jerry as it is declared jerry is in taskscope ]
    this is jerry in task scope
    ===>
    ~~SubStep2: [trace:  ]
    Trace:===>
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "remember that the caller's vars should override callee's vars\nso jerry's value should the one from caller instead this local value\n",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "<==="
        },
        {
          "name": "trace",
          "cmd": "--->"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "jerry": "jerry is overriden in local scope"
      },
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
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    }
    
    
    reverent_darwin4: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    {{.jerry}}
    ~~SubStep1: [print: remember that the caller's vars should override callee's vars
    so jerry's value should the one from caller instead this local value
     ]
    this is jerry in task scope
    <===
    ~~SubStep2: [trace:  ]
    Trace:<===
    --->
    ~~SubStep3: [trace:  ]
    Trace:--->
    --Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "this should print out the jerry defined in caller's task var scope",
          "cmd": "{{.jerry}}"
        },
        {
          "name": "trace",
          "cmd": "<---"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope",
      "tom": "this is tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1,
      "jerry": "this is jerry in task scope"
    }
    
    
    reverent_darwin4: overall final exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in task scope",
      "tom": "this is tom",
      "up_runtime_task_layer_number": 1
    })
    
    {{.jerry}}
    ~~SubStep1: [print: this should print out the jerry defined in caller's task var scope ]
    this is jerry in task scope
    <---
    ~~SubStep2: [trace:  ]
    Trace:<---
    
```

##### Logs with different verbose level
* [c0109 log - verbose level v](../../logs/c0109_v)
* [c0109 log - verbose level vv](../../logs/c0109_vv)
* [c0109 log - verbose level vvv](../../logs/c0109_vvv)
* [c0109 log - verbose level vvvv](../../logs/c0109_vvvv)
* [c0109 log - verbose level vvvvv](../../logs/c0109_vvvvv)

##### References
* [Related Chapter](../../vars/c0109)
