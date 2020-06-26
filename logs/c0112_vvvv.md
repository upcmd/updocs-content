---
title: "c0112_vvvv"
date: 2020-06-27T03:09:29+66:00
draft: false
weight: 11123

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0112
                 Verbose -> vvvv
              ModuleName -> clever_cray2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0112
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [clever_cray2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "global_b": "bbb",
      "global_a": "aaa"
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
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "tom": "my name is tom"
    })
    
    clever_cray2: overall final exec vars:
    
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
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa"
    })
    
    clever_cray2: overall final exec vars:
    
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1
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
      "global_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1,
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb"
    })
    
    clever_cray2: overall final exec vars:
    
    (*core.Cache)({
      "global_a": "aaa",
      "local_a": "aaa",
      "local_b": "bbb",
      "global_b": "bbb",
      "tom": "my name is tom",
      "up_runtime_task_layer_number": 1
    })
    
    ~~SubStep1: [print:  ]
    my name is tom
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    --Step3:
    {
      Name: "",
      Do: {
        "subtask2"
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
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1,
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb"
    })
    
    clever_cray2: overall final exec vars:
    
    (*core.Cache)({
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [subtask2]: 
    ==Task3: [task/subtask1 ==> subtask2:  ]
    Executing task stack layer: 3
    
    ---Step1:
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
      "local_b": "bbb",
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 2
    })
    
    clever_cray2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "my name is tom",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 2,
      "local_b": "bbb"
    })
    
    ~~~SubStep1: [print:  ]
    my name is tom
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    ---Step2:
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
      "local_b": "bbb",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 2
    })
    
    clever_cray2: overall final exec vars:
    
    (*core.Cache)({
      "tom": "my name is tom",
      "local_b": "bbb",
      "global_b": "bbb",
      "global_a": "aaa",
      "local_a": "aaa",
      "up_runtime_task_layer_number": 2
    })
    
    ~~~SubStep1: [print:  ]
    my name is tom
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .tom "my name is tom"}}]
    
```

##### Logs with different verbose level
* [c0112 log - verbose level v](../../logs/c0112_v)
* [c0112 log - verbose level vv](../../logs/c0112_vv)
* [c0112 log - verbose level vvv](../../logs/c0112_vvv)
* [c0112 log - verbose level vvvv](../../logs/c0112_vvvv)
* [c0112 log - verbose level vvvvv](../../logs/c0112_vvvvv)

##### References
* [Related Chapter](../../call-func/c0112)
