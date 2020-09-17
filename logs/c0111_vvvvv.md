---
title: "c0111_vvvvv"
date: 2020-09-18T01:27:40+99:00
draft: false
weight: 11114

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0111
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0111
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001752e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "global_a": "aaa",
      "global_b": "bbb"
    }
    
    (core.Cache) (len=2) {
     (string) (len=8) "global_a": (string) (len=3) "aaa",
     (string) (len=8) "global_b": (string) (len=3) "bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "global_a": "aaa",
      "global_b": "bbb"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "subtask1"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "local_b": "bbb",
        "tom": "my name is tom",
        "local_a": "aaa"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 0,
      "local_a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 0,
      "local_a": "aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 0,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
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
          "cmd": "{{.tom}}"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .tom \"my name is tom\"}}"
          }
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    })
    
    {{.tom}}
    ~~SubStep1: [print:  ]
    my name is tom
    [{{eq .tom "my name is tom"}}]
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    --Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.tom}}"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .tom \"my name is tom\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "tom": "hi i am tom"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "my name is tom",
      "global_a": "aaa",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_a": "aaa"
    })
    
    {{.tom}}
    ~~SubStep1: [print:  ]
    my name is tom
    [{{eq .tom "my name is tom"}}]
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    
```

##### Logs with different verbose level
* [c0111 log - verbose level v](../../logs/c0111_v)
* [c0111 log - verbose level vv](../../logs/c0111_vv)
* [c0111 log - verbose level vvv](../../logs/c0111_vvv)
* [c0111 log - verbose level vvvv](../../logs/c0111_vvvv)
* [c0111 log - verbose level vvvvv](../../logs/c0111_vvvvv)

##### References
* [Related Chapter](../../call-func/c0111)
