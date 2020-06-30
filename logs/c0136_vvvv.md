---
title: "c0136_vvvv"
date: 2020-07-01T15:34:40+77:00
draft: false
weight: 11363

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0136
                 Verbose -> vvvv
              ModuleName -> backstabbing_newton1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0136
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [backstabbing_newton1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "callee_task1"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "local_aaa",
        "b": "local_bbb"
      },
      Dvars: {
        {
          Name: "da",
          Value: "local_da",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "db",
          Value: "local_db",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    backstabbing_newton1: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    })
    
      located task-> 3 [callee_task1]: 
    =Task3: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "callee_task2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "local_aaa_callee_task1",
        "b": "local_bbb_callee_task1"
      },
      Dvars: {
        {
          Name: "da",
          Value: "local_da_callee_task1",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "db",
          Value: "local_db_callee_task1",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
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
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 1,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    backstabbing_newton1: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 1,
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1"
    })
    
      located task-> 2 [callee_task2]: 
    ==Task2: [task/callee_task1 ==> callee_task2:  ]
    Executing task stack layer: 3
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "a: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"local_aaa\" }}",
                "{{eq .b \"local_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da_callee_task1\" }}",
                "{{eq .db \"callee_db_callee_task2\" }}"
              },
              "flags": {
                "failfast"
              }
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "a": "callee_aaa_callee_task2"
      },
      Dvars: {
        {
          Name: "db",
          Value: "callee_db_callee_task2",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
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
      "up_runtime_task_layer_number": 2,
      "b": "local_bbb",
      "da": "local_da_callee_task1",
      "a": "local_aaa",
      "db": "local_db_callee_task1",
      "c": "global_ccc"
    })
    
    backstabbing_newton1: overall final exec vars:
    
    (*core.Cache)({
      "da": "local_da_callee_task1",
      "a": "local_aaa",
      "db": "callee_db_callee_task2",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 2,
      "b": "local_bbb"
    })
    
    ---Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "a: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n",
          "name": "print"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"local_aaa\" }}",
            "{{eq .b \"local_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da_callee_task1\" }}",
            "{{eq .db \"callee_db_callee_task2\" }}"
          },
          "flags": {
            "failfast"
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
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 2,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    backstabbing_newton1: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 2,
      "a": "local_aaa"
    })
    
    ~~~SubStep1: [print:  ]
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da_callee_task1
    db: callee_db_callee_task2
    
    ~~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "local_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da_callee_task1" }}]
     5 ASSERT OK:     [{{eq .db "callee_db_callee_task2" }}]
    
```

##### Logs with different verbose level
* [c0136 log - verbose level v](../../logs/c0136_v)
* [c0136 log - verbose level vv](../../logs/c0136_vv)
* [c0136 log - verbose level vvv](../../logs/c0136_vvv)
* [c0136 log - verbose level vvvv](../../logs/c0136_vvvv)
* [c0136 log - verbose level vvvvv](../../logs/c0136_vvvvv)

##### References
* [Related Chapter](../../block-func/c0136)
