---
title: "c0113_vvvvv"
date: 2020-08-09T01:36:16+88:00
draft: false
weight: 11134

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0113
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
    loading [Task]:  ./tests/functests/c0113
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed4e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
    (core.Cache) (len=2) {
     (string) (len=3) "tom": (string) (len=21) "this is tom in global",
     (string) (len=5) "jerry": (string) (len=23) "this is jerry in global"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: call subtask and exam the return value in following steps ]
    {
      Name: "",
      Do: "subtask",
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
      "jerry": "this is jerry in global",
      "tom": "this is tom in global"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
    caller's vars to task (subtask)::
    (*core.Cache)({
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [: check value of tom after it is registered in current task stack ]
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "desc": "by default hitom is registered in to global context",
          "cmd": {
            "value": "tom created in sub_loop",
            "name": "tom"
          }
        },
        {
          "name": "print",
          "cmd": "in sub_loop print1: {{.tom}}"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .tom \"tom created in sub_loop\"}}"
          }
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
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "tom": "this is tom in global",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    map[name:tom value:tom created in sub_loop]
    ~~SubStep1: [reg: by default hitom is registered in to global context ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "tom": "tom created in sub_loop",
      "jerry": "this is jerry in global"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "john": "john in sub_loop func1",
      "tom": "tom created in sub_loop",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    in sub_loop print1: {{.tom}}
    ~~SubStep2: [print:  ]
    in sub_loop print1: tom created in sub_loop
    [{{eq .tom "tom created in sub_loop"}}]
    ~~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    --Step2: [: check value of tom and it should be available in current stack ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in sub_loop print2: {{.tom}}"
        },
        {
          "name": "assert",
          "desc": "since .tom is in callee's global, it should be accessible here",
          "cmd": {
            "{{eq .tom \"tom created in sub_loop\"}}"
          }
        },
        {
          "name": "return",
          "desc": "it should return and merge tom to parent's vars scope\nit should report warning as jason does not exist\n",
          "cmd": {
            "tom",
            "jason"
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
      "tom": "tom created in sub_loop",
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in sub_loop"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "john": "john in sub_loop func2",
      "jerry": "this is jerry in global",
      "up_runtime_task_layer_number": 1,
      "tom": "tom created in sub_loop"
    })
    
    in sub_loop print2: {{.tom}}
    ~~SubStep1: [print:  ]
    in sub_loop print2: tom created in sub_loop
    [{{eq .tom "tom created in sub_loop"}}]
    ~~SubStep2: [assert: since .tom is in callee's global, it should be accessible here ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    [tom jason]
    ~~SubStep3: [return: it should return and merge tom to parent's vars scope
    it should report warning as jason does not exist
     ]
     WARN: [return validation] - [The referencing var name: (jason) not exist]
    contextual return vars:
    
    (*core.Cache)({
      "tom": "tom created in sub_loop"
    })
    
    -Step2: [: check value of tom ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "in main task print3: {{.tom}}"
        },
        {
          "name": "assert",
          "desc": "since .tom is returned from callee, it should be accessible here",
          "cmd": {
            "{{eq .tom \"tom created in sub_loop\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "check value of tom",
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
      "tom": "tom created in sub_loop",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "jerry": "this is jerry in global",
      "tom": "tom created in sub_loop",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "jerry": "this is jerry in global",
      "tom": "tom created in sub_loop",
      "up_runtime_task_layer_number": 1
    })
    
    in main task print3: {{.tom}}
    ~SubStep1: [print:  ]
    in main task print3: tom created in sub_loop
    [{{eq .tom "tom created in sub_loop"}}]
    ~SubStep2: [assert: since .tom is returned from callee, it should be accessible here ]
     1 ASSERT OK:     [{{eq .tom "tom created in sub_loop"}}]
    
```

##### Logs with different verbose level
* [c0113 log - verbose level v](../../logs/c0113_v)
* [c0113 log - verbose level vv](../../logs/c0113_vv)
* [c0113 log - verbose level vvv](../../logs/c0113_vvv)
* [c0113 log - verbose level vvvv](../../logs/c0113_vvvv)
* [c0113 log - verbose level vvvvv](../../logs/c0113_vvvvv)

##### References
* [Related Chapter](../../call-func/c0113)
