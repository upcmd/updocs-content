---
title: "c0115_vvvvv"
date: 2020-10-07T00:11:20+1010:00
draft: false
weight: 11154

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0115
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0115
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000aad60)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    })
    
    (*core.Cache)(0xc0000c6150)((len=2) {
     (string) (len=5) "jerry": (string) (len=23) "this is jerry in global",
     (string) (len=3) "tom": (string) (len=21) "this is tom in global"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [main task: call subtask and exam the return value in following steps ]
    {
      Name: "main task",
      Do: "subtask1",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "call subtask and exam the return value in following steps",
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
      "up_runtime_task_layer_number": 0,
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 2 [subtask1]: 
    =Task2: [task ==> subtask1: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom after it is registered in current task stack ]
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "desc": "by default hitom is registered in to global context",
          "cmd": {
            "name": "tom",
            "value": "tom created in subtask1"
          }
        },
        {
          "name": "print",
          "cmd": "in subtask1 print1: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub_loop func1"
      },
      Dvars: <nil>,
      Desc: "check value of tom after it is registered in current task stack",
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
      "jerry": "this is jerry in global",
      "john": "john in sub_loop func1",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "john": "john in sub_loop func1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "up_runtime_task_layer_number": 1,
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    map[name:tom value:tom created in subtask1]
    ~~SubStep1: [reg: by default hitom is registered in to global context ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 0
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global",
      "john": "john in sub_loop func1"
    })
    
    in subtask1 print1: {{.tom}}
    ~~SubStep2: [print:  ]
    in subtask1 print1: tom created in subtask1
    --Step2: [: check value of tom and it should be available in current stack ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in subtask1 print21: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub_loop func2"
      },
      Dvars: <nil>,
      Desc: "check value of tom and it should be available in current stack",
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
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2",
      "tom": "tom created in subtask1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func2",
      "tom": "tom created in subtask1"
    })
    
    in subtask1 print21: {{.tom}}
    ~~SubStep1: [print:  ]
    in subtask1 print21: tom created in subtask1
    --Step3: [: call subtask and exam the return value in following steps ]
    {
      Name: "",
      Do: {
        "subtask2",
        "subtask3"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "call subtask and exam the return value in following steps",
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
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global"
    })
    
    caller's vars to task (subtask2)::
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in subtask1"
    })
    
      located task-> 3 [subtask2]: 
    ==Task3: [task/subtask1 ==> subtask2: subtask to test reg and return ]
    Executing task stack layer: 3
    
    ---Step1: [: check value of tom after it is registered in current task stack ]
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "desc": "by default hitom is registered in to global context",
          "cmd": {
            "name": "tom",
            "value": "tom2 created in subtask2"
          }
        },
        {
          "name": "print",
          "cmd": "in subtask2 print1: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub_loop func1"
      },
      Dvars: <nil>,
      Desc: "check value of tom after it is registered in current task stack",
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
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func1",
      "tom": "tom created in subtask1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom created in subtask1",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func1"
    })
    
    map[name:tom value:tom2 created in subtask2]
    ~~~SubStep1: [reg: by default hitom is registered in to global context ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func1",
      "tom": "tom2 created in subtask2"
    })
    
    in subtask2 print1: {{.tom}}
    ~~~SubStep2: [print:  ]
    in subtask2 print1: tom2 created in subtask2
    ---Step2: [: check value of tom and it should be available in current stack ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in subtask2 print2: {{.tom}}"
        },
        {
          "name": "return",
          "cmd": {
            "tom"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub_loop func2"
      },
      Dvars: <nil>,
      Desc: "check value of tom and it should be available in current stack",
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
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "tom": "tom2 created in subtask2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "tom": "tom2 created in subtask2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "tom": "tom2 created in subtask2"
    })
    
    in subtask2 print2: {{.tom}}
    ~~~SubStep1: [print:  ]
    in subtask2 print2: tom2 created in subtask2
    [tom]
    ~~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "tom": "tom2 created in subtask2"
    })
    
    caller's vars to task (subtask3)::
    (*core.Cache)({
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 4 [subtask3]: 
    ==Task4: [task/subtask1 ==> subtask3: subtask3 ]
    Executing task stack layer: 3
    
    ---Step1: [: dummy ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "dummy to help build inspect task"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "dummy",
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
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2,
      "tom": "tom2 created in subtask2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    })
    
    dummy to help build inspect task
    ~~~SubStep1: [print:  ]
    dummy to help build inspect task
    --Step4: [: check value of tom and it should be available in current stack ]
    {
      Name: "",
      Do: {
        {
          "cmd": "in subtask1 print22: {{.tom}}",
          "name": "print"
        },
        {
          "name": "return",
          "cmd": {
            "tom"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "john": "john in sub_loop func2"
      },
      Dvars: <nil>,
      Desc: "check value of tom and it should be available in current stack",
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
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 2,
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    })
    
    in subtask1 print22: {{.tom}}
    ~~SubStep1: [print:  ]
    in subtask1 print22: tom2 created in subtask2
    [tom]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "tom": "tom2 created in subtask2"
    })
    
    -Step2: [
    check value of tom
    in this case tom's value should come from subtask1
    tom's expected value:  tom created in subtask1
    ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in main task print3: {{.tom}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "check value of tom\nin this case tom's value should come from subtask1\ntom's expected value:  tom created in subtask1\n",
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
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "tom2 created in subtask2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 2
    })
    
    in main task print3: {{.tom}}
    ~SubStep1: [print:  ]
    in main task print3: tom2 created in subtask2
    
```

##### Logs with different verbose level
* [c0115 log - verbose level v](../../logs/c0115_v)
* [c0115 log - verbose level vv](../../logs/c0115_vv)
* [c0115 log - verbose level vvv](../../logs/c0115_vvv)
* [c0115 log - verbose level vvvv](../../logs/c0115_vvvv)
* [c0115 log - verbose level vvvvv](../../logs/c0115_vvvvv)

##### References
* [Related Chapter](../../call-func/c0115)
