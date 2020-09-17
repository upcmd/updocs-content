---
title: "c0130_vvvvv"
date: 2020-09-18T00:51:45+99:00
draft: false
weight: 11304

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0130
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
    loading [Task]:  ./tests/functests/c0130
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf760)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "goahead": false,
      "a": "global_aaa",
      "b": "global_bbb",
      "c": "global_ccc"
    }
    
    (core.Cache) (len=4) {
     (string) (len=7) "goahead": (bool) false,
     (string) (len=1) "a": (string) (len=10) "global_aaa",
     (string) (len=1) "b": (string) (len=10) "global_bbb",
     (string) (len=1) "c": (string) (len=10) "global_ccc"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "goahead": false,
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
          "do": {
            {
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n",
              "name": "print"
            }
          },
          "func": "cmd",
          "vars": {
            "a": "block_layer1_aaa"
          }
        },
        {
          "func": "shell",
          "do": {
            "echo \"shell step3\"",
            "echo \"shell step4\""
          }
        },
        {
          "do": {
            {
              "do": {
                {
                  "name": "print",
                  "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
                }
              },
              "func": "cmd",
              "vars": {
                "a": "block_layer2_aaa"
              }
            }
          },
          "func": "block",
          "desc": "test embeded 2nd layer of block",
          "vars": {
            "b": "local_block_layer2_bbb",
            "a": "local_block_layer2_aaa"
          },
          "dvars": {
            {
              "name": "da",
              "value": "local_da_layer2"
            },
            {
              "value": "local_db_layer2",
              "name": "db"
            }
          }
        },
        {
          "func": "shell",
          "do": {
            "echo \"shell step5\"",
            "echo \"shell step6\""
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
      If: "{{.goahead}}",
      Else: {
        {
          "func": "shell",
          "do": {
            "echo \"else step1\"",
            "echo \"else step2\""
          }
        },
        {
          "func": "cmd",
          "vars": {
            "a": "block_layer1_aaa_else"
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            }
          }
        }
      },
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
      "goahead": false,
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
      "goahead": false,
      "da": "local_da",
      "db": "local_db",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"else step1\"",
        "echo \"else step2\""
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
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "a": "local_aaa",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    })
    
    cmd( 1):
    echo "else step1"
    
    cmd=>:
    echo "else step1"
    -
    else step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"else step1\"",
     Code: (int) 0,
     Output: (string) (len=10) "else step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "else step2"
    
    cmd=>:
    echo "else step2"
    -
    else step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"else step2\"",
     Code: (int) 0,
     Output: (string) (len=10) "else step2",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "block_layer1_aaa_else"
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
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "db": "local_db",
      "c": "global_ccc",
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "goahead": false,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"else step2\"",
        Code: 0,
        Output: "else step2",
        ErrMsg: ""
      }),
      "a": "block_layer1_aaa_else",
      "b": "local_bbb",
      "up_runtime_task_layer_number": 0,
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
    })
    
    layer 1
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: 0
    a: block_layer1_aaa_else
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db
    
    
```

##### Logs with different verbose level
* [c0130 log - verbose level v](../../logs/c0130_v)
* [c0130 log - verbose level vv](../../logs/c0130_vv)
* [c0130 log - verbose level vvv](../../logs/c0130_vvv)
* [c0130 log - verbose level vvvv](../../logs/c0130_vvvv)
* [c0130 log - verbose level vvvvv](../../logs/c0130_vvvvv)

##### References
* [Related Chapter](../../block-func/c0130)
