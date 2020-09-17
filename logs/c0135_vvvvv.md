---
title: "c0135_vvvvv"
date: 2020-09-18T01:27:46+99:00
draft: false
weight: 11354

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0135
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
    loading [Task]:  ./tests/functests/c0135
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed380)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "c": "global_ccc",
      "a": "global_aaa",
      "b": "global_bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "c": (string) (len=10) "global_ccc",
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
      located task-> 2 [task]: 
    Task2: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "callee_task"
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
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db",
      "da": "local_da"
    }
    
    
    scope[local] merged: {
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da"
    })
    
    caller's vars to task (callee_task)::
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "db": "local_db",
      "da": "local_da"
    })
    
      located task-> 1 [callee_task]: 
    =Task1: [task ==> callee_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "do": {
            {
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n",
              "name": "print"
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"local_aaa\" }}",
                "{{eq .b \"local_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da\" }}",
                "{{eq .db \"callee_db\" }}"
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
        "a": "callee_aaa"
      },
      Dvars: {
        {
          Name: "db",
          Value: "callee_db",
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
      "c": "global_ccc",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "local_db",
      "da": "local_da",
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
      "db": "callee_db"
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "a": "local_aaa",
      "c": "global_ccc",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "c": "global_ccc",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db",
      "da": "local_da"
    })
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"local_aaa\" }}",
            "{{eq .b \"local_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da\" }}",
            "{{eq .db \"callee_db\" }}"
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
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db",
      "da": "local_da",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db",
      "da": "local_da"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db",
      "da": "local_da"
    })
    
    layer 1
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 1
    a: local_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: callee_db
    
    [{{eq .a "local_aaa" }} {{eq .b "local_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da" }} {{eq .db "callee_db" }}]
    ~~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "local_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "callee_db" }}]
    
```

##### Logs with different verbose level
* [c0135 log - verbose level v](../../logs/c0135_v)
* [c0135 log - verbose level vv](../../logs/c0135_vv)
* [c0135 log - verbose level vvv](../../logs/c0135_vvv)
* [c0135 log - verbose level vvvv](../../logs/c0135_vvvv)
* [c0135 log - verbose level vvvvv](../../logs/c0135_vvvvv)

##### References
* [Related Chapter](../../block-func/c0135)
