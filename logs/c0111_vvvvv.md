---
title: "c0111_vvvvv"
date: 2020-07-01T15:34:36+77:00
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
              ModuleName -> distracted_jones2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0111
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001812a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [distracted_jones2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "global_b": "bbb",
      "global_a": "aaa"
    }
    
    (core.Cache) (len=2) {
     (string) (len=8) "global_b": (string) (len=3) "bbb",
     (string) (len=8) "global_a": (string) (len=3) "aaa"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "global_b": "bbb",
      "global_a": "aaa"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb"
    }
    
    
    distracted_jones2: overall final exec vars:
    
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa"
    })
    
    caller's vars to task (subtask1)::
    (*core.Cache)({
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb"
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
          "cmd": {
            "{{eq .tom \"my name is tom\"}}"
          },
          "name": "assert"
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
      "tom": "my name is tom",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb"
    }
    
    
    distracted_jones2: overall final exec vars:
    
    (*core.Cache)({
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "local_b": "bbb",
      "global_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "local_a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "global_b": "bbb"
    }
    
    
    distracted_jones2: overall final exec vars:
    
    (*core.Cache)({
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "global_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1
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
