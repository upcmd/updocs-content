---
title: "c0133_vvvvv"
date: 2020-06-25T01:56:04+66:00
draft: false
weight: 11334

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0133
                 Verbose -> vvvvv
              ModuleName -> agitated_euclid6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0133
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef7c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [agitated_euclid6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "b": (string) (len=10) "global_bbb",
     (string) (len=1) "c": (string) (len=10) "global_ccc",
     (string) (len=1) "a": (string) (len=10) "global_aaa"
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
          "vars": {
            "a": "block_layer1_aaa"
          },
          "dvars": {
            {
              "name": "db",
              "value": "local_db_layer1"
            }
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            },
            {
              "name": "assert",
              "cmd": {
                "{{eq .a \"block_layer1_aaa\" }}",
                "{{eq .b \"local_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da\" }}",
                "{{eq .db \"local_db_layer1\" }}"
              },
              "flags": {
                "failfast"
              }
            }
          },
          "func": "cmd"
        },
        {
          "do": {
            "echo \"shell step3\"",
            "echo \"shell step4\""
          },
          "func": "shell"
        },
        {
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
              "name": "db",
              "value": "local_db_layer2"
            }
          },
          "do": {
            {
              "vars": {
                "a": "block_layer2_aaa"
              },
              "do": {
                {
                  "name": "print",
                  "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
                },
                {
                  "flags": {
                    "failfast"
                  },
                  "name": "assert",
                  "cmd": {
                    "{{eq .a \"block_layer2_aaa\" }}",
                    "{{eq .b \"local_block_layer2_bbb\" }}",
                    "{{eq .c \"global_ccc\" }}",
                    "{{eq .da \"local_da_layer2\" }}",
                    "{{eq .db \"local_db_layer2\" }}"
                  }
                }
              },
              "func": "cmd"
            }
          }
        },
        {
          "do": {
            "echo \"shell step5\"",
            "echo \"shell step6\""
          },
          "func": "shell"
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
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da",
      "db": "local_db"
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db",
      "da": "local_da"
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db",
      "da": "local_da"
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
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "da": "local_da",
      "db": "local_db"
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
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
          "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"block_layer1_aaa\" }}",
            "{{eq .b \"local_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da\" }}",
            "{{eq .db \"local_db_layer1\" }}"
          },
          "flags": {
            "failfast"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "block_layer1_aaa"
      },
      Dvars: {
        {
          Name: "db",
          Value: "local_db_layer1",
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
      "db": "local_db_layer1"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db_layer1",
      "da": "local_da",
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "c": "global_ccc"
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "db": "local_db_layer1",
      "da": "local_da",
      "a": "block_layer1_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      })
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
    up_runtime_task_layer_number: <no value>
    a: block_layer1_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db_layer1
    
    [{{eq .a "block_layer1_aaa" }} {{eq .b "local_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da" }} {{eq .db "local_db_layer1" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer1_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer1" }}]
    -Step3:
    {
      Name: "",
      Do: {
        "echo \"shell step3\"",
        "echo \"shell step4\""
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
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "da": "local_da",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db"
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "da": "local_da",
      "a": "local_aaa",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "db": "local_db"
    })
    
    cmd( 1):
    echo "shell step3"
    
     \_ echo "shell step3"
    shell step3
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step3",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step4"
    
     \_ echo "shell step4"
    shell step4
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step4",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step4: [: test embeded 2nd layer of block ]
    {
      Name: "",
      Do: {
        {
          "vars": {
            "a": "block_layer2_aaa"
          },
          "do": {
            {
              "name": "print",
              "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
            },
            {
              "cmd": {
                "{{eq .a \"block_layer2_aaa\" }}",
                "{{eq .b \"local_block_layer2_bbb\" }}",
                "{{eq .c \"global_ccc\" }}",
                "{{eq .da \"local_da_layer2\" }}",
                "{{eq .db \"local_db_layer2\" }}"
              },
              "flags": {
                "failfast"
              },
              "name": "assert"
            }
          },
          "func": "cmd"
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: {
        "a": "local_block_layer2_aaa",
        "b": "local_block_layer2_bbb"
      },
      Dvars: {
        {
          Name: "da",
          Value: "local_da_layer2",
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
          Value: "local_db_layer2",
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
      Desc: "test embeded 2nd layer of block",
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
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db",
      "da": "local_da",
      "a": "local_block_layer2_aaa"
    })
    
    [local] dvar expanded result:
    {
      "da": "local_da_layer2",
      "db": "local_db_layer2"
    }
    
    
    scope[local] merged: {
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db_layer2",
      "da": "local_da_layer2",
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb"
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "da": "local_da_layer2",
      "a": "local_block_layer2_aaa",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "db": "local_db_layer2"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .a \"block_layer2_aaa\" }}",
            "{{eq .b \"local_block_layer2_bbb\" }}",
            "{{eq .c \"global_ccc\" }}",
            "{{eq .da \"local_da_layer2\" }}",
            "{{eq .db \"local_db_layer2\" }}"
          },
          "flags": {
            "failfast"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "block_layer2_aaa"
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
      "db": "local_db_layer2",
      "da": "local_da_layer2",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "a": "block_layer2_aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "block_layer2_aaa",
      "db": "local_db_layer2",
      "da": "local_da_layer2",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      })
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "a": "block_layer2_aaa",
      "db": "local_db_layer2",
      "da": "local_da_layer2"
    })
    
    layer 2
    up_runtime_task_layer_number: {{.up_runtime_task_layer_number}}
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    da: {{.da}}
    db: {{.db}}
    
    ~SubStep1: [print:  ]
    layer 2
    up_runtime_task_layer_number: <no value>
    a: block_layer2_aaa
    b: local_block_layer2_bbb
    c: global_ccc
    da: local_da_layer2
    db: local_db_layer2
    
    [{{eq .a "block_layer2_aaa" }} {{eq .b "local_block_layer2_bbb" }} {{eq .c "global_ccc" }} {{eq .da "local_da_layer2" }} {{eq .db "local_db_layer2" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .a "block_layer2_aaa" }}]
     2 ASSERT OK:     [{{eq .b "local_block_layer2_bbb" }}]
     3 ASSERT OK:     [{{eq .c "global_ccc" }}]
     4 ASSERT OK:     [{{eq .da "local_da_layer2" }}]
     5 ASSERT OK:     [{{eq .db "local_db_layer2" }}]
    -Step5:
    {
      Name: "",
      Do: {
        "echo \"shell step5\"",
        "echo \"shell step6\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da",
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      })
    }
    
    
    agitated_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "a": "local_aaa",
      "db": "local_db",
      "da": "local_da"
    })
    
    cmd( 1):
    echo "shell step5"
    
     \_ echo "shell step5"
    shell step5
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step5",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "shell step6"
    
     \_ echo "shell step6"
    shell step6
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "shell step6",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0133 log - verbose level v](../../logs/c0133_v)
* [c0133 log - verbose level vv](../../logs/c0133_vv)
* [c0133 log - verbose level vvv](../../logs/c0133_vvv)
* [c0133 log - verbose level vvvv](../../logs/c0133_vvvv)
* [c0133 log - verbose level vvvvv](../../logs/c0133_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0133)