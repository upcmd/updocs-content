---
title: "c0136_vvvvv"
date: 2020-08-18T15:16:16+88:00
draft: false
weight: 11364

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
    loading [Task]:  ./tests/functests/c0136
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002695a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb",
     (string) (len=1) "c": (string) (len=10) "global_ccc"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db",
      "da": "local_da"
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    caller's vars to task (callee_task1)::
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "up_runtime_task_layer_number": 1,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1",
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (callee_task2)::
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1",
      "up_runtime_task_layer_number": 1
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
                "failFast"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "local_db_callee_task1",
      "up_runtime_task_layer_number": 2,
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
      "db": "callee_db_callee_task2"
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "up_runtime_task_layer_number": 2,
      "b": "local_bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "callee_db_callee_task2",
      "up_runtime_task_layer_number": 2,
      "b": "local_bbb",
      "a": "local_aaa",
      "c": "global_ccc",
      "da": "local_da_callee_task1"
    })
    
    ---Step1:
    {
      Name: "",
      Do: {
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
            "failFast"
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
      "up_runtime_task_layer_number": 2,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "db": "callee_db_callee_task2",
      "up_runtime_task_layer_number": 2,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da_callee_task1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "da": "local_da_callee_task1",
      "db": "callee_db_callee_task2",
      "up_runtime_task_layer_number": 2,
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~~~SubStep1: [print:  ]
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da_callee_task1
    db: callee_db_callee_task2
    
    [{{eq .a "local_aaa" }} {{eq .b "local_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da_callee_task1" }} {{eq .db "callee_db_callee_task2" }}]
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
