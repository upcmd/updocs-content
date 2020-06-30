---
title: "c0128_vvvvv"
date: 2020-07-01T15:34:39+77:00
draft: false
weight: 11284

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0128
                 Verbose -> vvvvv
              ModuleName -> tender_bohr9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0128
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef100)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [tender_bohr9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
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
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: show example the route goes to call goelse for the condition of not if condition succeeds ]
    {
      Name: "",
      Do: {
        {
          "func": "shell",
          "do": {
            "echo \"shell step1\"",
            "echo \"shell step2\""
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "cmd print step\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nda: {{.da}}\ndb: {{.db}}\n"
            }
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
      Desc: "show example the route goes to call goelse for the condition of not if condition succeeds",
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
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da"
    }
    
    
    tender_bohr9: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"shell step1\"",
        "echo \"shell step2\""
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb"
    }
    
    
    tender_bohr9: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db"
    })
    
    cmd( 1):
    echo "shell step1"
    
     \_ echo "shell step1"
    shell step1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step2"
    
     \_ echo "shell step2"
    shell step2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step2",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "cmd print step\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nda: {{.da}}\ndb: {{.db}}\n"
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
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
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
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da"
    }
    
    
    tender_bohr9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    cmd print step
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    da: {{.da}}
    db: {{.db}}
    
    ~SubStep1: [print:  ]
    cmd print step
    up_runtime_task_layer_number: <no value>
    a: local_aaa
    b: local_bbb
    da: local_da
    db: local_db
    
    
```

##### Logs with different verbose level
* [c0128 log - verbose level v](../../logs/c0128_v)
* [c0128 log - verbose level vv](../../logs/c0128_vv)
* [c0128 log - verbose level vvv](../../logs/c0128_vvv)
* [c0128 log - verbose level vvvv](../../logs/c0128_vvvv)
* [c0128 log - verbose level vvvvv](../../logs/c0128_vvvvv)

##### References
* [Related Chapter](../../block-func/c0128)
