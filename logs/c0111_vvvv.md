---
title: "c0111_vvvv"
date: 2020-06-25T01:55:59+66:00
draft: false
weight: 11113

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
                 Verbose -> vvvv
              ModuleName -> stoic_stallman4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0111
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [stoic_stallman4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "global_b": "bbb",
      "global_a": "aaa"
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
        "local_a": "aaa",
        "local_b": "bbb",
        "tom": "my name is tom"
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
    
    stoic_stallman4: overall final exec vars:
    
    (*core.Cache)({
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb"
    })
    
    stoic_stallman4: overall final exec vars:
    
    (*core.Cache)({
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb"
    })
    
    ~~SubStep1: [print:  ]
    my name is tom
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
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb"
    })
    
    stoic_stallman4: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa"
    })
    
    ~~SubStep1: [print:  ]
    my name is tom
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