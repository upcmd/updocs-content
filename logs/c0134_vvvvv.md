---
title: "c0134_vvvvv"
date: 2020-07-01T15:34:40+77:00
draft: false
weight: 11344

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0134
                 Verbose -> vvvvv
              ModuleName -> pensive_hawking6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0134
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb400)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [pensive_hawking6] instance id: [dev]
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
        {
          "func": "shell",
          "do": {
            "echo \"in block\""
          }
        },
        {
          "func": "call",
          "do": {
            "callee_task"
          }
        }
      },
      Dox: <nil>,
      Func: "block",
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
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db",
      "da": "local_da"
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
    }
    
    
    pensive_hawking6: overall final exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"in block\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    }
    
    
    pensive_hawking6: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
    })
    
    cmd( 1):
    echo "in block"
    
     \_ echo "in block"
    in block
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=8) "in block",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "callee_task"
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      })
    }
    
    
    pensive_hawking6: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    })
    
    caller's vars to task (callee_task)::
    (*core.Cache)({
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      })
    })
    
      located task-> 2 [callee_task]: 
    =Task2: [task ==> callee_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        },
        {
          "flags": {
            "failfast"
          },
          "name": "assert",
          "cmd": {
            "{{eq .a \"local_aaa\" }}",
            "{{eq .b \"local_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da\" }}",
            "{{eq .db \"callee_db\" }}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "da": "local_da",
      "up_runtime_task_layer_number": 1,
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
      "db": "callee_db"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "da": "local_da",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    }
    
    
    pensive_hawking6: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "da": "local_da",
      "up_runtime_task_layer_number": 1,
      "db": "callee_db"
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
* [c0134 log - verbose level v](../../logs/c0134_v)
* [c0134 log - verbose level vv](../../logs/c0134_vv)
* [c0134 log - verbose level vvv](../../logs/c0134_vvv)
* [c0134 log - verbose level vvvv](../../logs/c0134_vvvv)
* [c0134 log - verbose level vvvvv](../../logs/c0134_vvvvv)

##### References
* [Related Chapter](../../block-func/c0134)
