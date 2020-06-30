---
title: "c0129_vvvv"
date: 2020-07-01T15:34:39+77:00
draft: false
weight: 11293

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0129
                 Verbose -> vvvv
              ModuleName -> determined_heisenberg2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0129
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_heisenberg2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "b": "global_bbb",
      "c": "global_ccc",
      "a": "global_aaa"
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
              "name": "print",
              "cmd": "layer 1\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
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
          "vars": {
            "a": "local_block_layer2_aaa",
            "b": "local_block_layer2_bbb"
          },
          "dvars": {
            {
              "value": "local_da_layer2",
              "name": "da"
            },
            {
              "name": "db",
              "value": "local_db_layer2"
            }
          },
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
          "desc": "test embeded 2nd layer of block"
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
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
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
      "db": "local_db",
      "c": "global_ccc",
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da"
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "a": "local_aaa",
      "b": "local_bbb",
      "da": "local_da",
      "db": "local_db",
      "c": "global_ccc"
    })
    
    cmd( 1):
    echo "shell step1"
    
     \_ echo "shell step1"
    shell step1
     .. ok
    cmd( 2):
    echo "shell step2"
    
     \_ echo "shell step2"
    shell step2
     .. ok
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
        "a": "block_layer1_aaa"
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer1_aaa"
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "b": "local_bbb",
      "c": "global_ccc",
      "db": "local_db",
      "da": "local_da",
      "a": "block_layer1_aaa"
    })
    
    ~SubStep1: [print:  ]
    layer 1
    up_runtime_task_layer_number: <no value>
    a: block_layer1_aaa
    b: local_bbb
    c: global_ccc
    da: local_da
    db: local_db
    
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa"
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step2",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db"
    })
    
    cmd( 1):
    echo "shell step3"
    
     \_ echo "shell step3"
    shell step3
     .. ok
    cmd( 2):
    echo "shell step4"
    
     \_ echo "shell step4"
    shell step4
     .. ok
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da",
      "db": "local_db",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "a": "local_block_layer2_aaa"
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc",
      "a": "local_block_layer2_aaa"
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "layer 2\nup_runtime_task_layer_number: {{.up_runtime_task_layer_number}}\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\nda: {{.da}}\ndb: {{.db}}\n"
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
      "a": "block_layer2_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc"
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "a": "block_layer2_aaa",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      }),
      "da": "local_da_layer2",
      "db": "local_db_layer2",
      "b": "local_block_layer2_bbb",
      "c": "global_ccc"
    })
    
    ~SubStep1: [print:  ]
    layer 2
    up_runtime_task_layer_number: <no value>
    a: block_layer2_aaa
    b: local_block_layer2_bbb
    c: global_ccc
    da: local_da_layer2
    db: local_db_layer2
    
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
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      })
    })
    
    determined_heisenberg2: overall final exec vars:
    
    (*core.Cache)({
      "b": "local_bbb",
      "c": "global_ccc",
      "a": "local_aaa",
      "da": "local_da",
      "db": "local_db",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "shell step4",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "shell step5"
    
     \_ echo "shell step5"
    shell step5
     .. ok
    cmd( 2):
    echo "shell step6"
    
     \_ echo "shell step6"
    shell step6
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0129 log - verbose level v](../../logs/c0129_v)
* [c0129 log - verbose level vv](../../logs/c0129_vv)
* [c0129 log - verbose level vvv](../../logs/c0129_vvv)
* [c0129 log - verbose level vvvv](../../logs/c0129_vvvv)
* [c0129 log - verbose level vvvvv](../../logs/c0129_vvvvv)

##### References
* [Related Chapter](../../block-func/c0129)
