---
title: "c0134_vvvvv"
date: 2020-10-07T00:11:24+1010:00
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
    loading [Task]:  ./tests/functests/c0134
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf500)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    })
    
    (*core.Cache)(0xc00000e938)((len=3) {
     (string) (len=1) "c": (string) (len=10) "global_ccc",
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    })
    
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
        "b": "local_bbb",
        "a": "local_aaa"
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
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    })
    
    cmd( 1):
    echo "in block"
    
    cmd=>:
    echo "in block"
    -
    in block
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=15) "echo \"in block\"",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      })
    })
    
    caller's vars to task (callee_task)::
    (*core.Cache)({
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
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
            "failFast"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "a": "local_aaa"
    })
    
    [local] dvar expanded result:
    {
      "db": "callee_db"
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "db": "callee_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "a": "local_aaa",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "da": "local_da",
      "db": "callee_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"in block\"",
        Code: 0,
        Output: "in block",
        ErrMsg: ""
      }),
      "a": "local_aaa"
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
