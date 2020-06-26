---
title: "c0086_vvvvv"
date: 2020-06-27T03:09:25+66:00
draft: false
weight: 10864

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0086
                 Verbose -> vvvvv
              ModuleName -> fervent_mayer9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0086
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed5e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [fervent_mayer9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    (core.Cache) (len=1) {
     (string) (len=5) "lines": (string) (len=31) "hello\nthis\nis a\nbeautiful world"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo '{{.lines}}'",
        "echo '{{.linelist}}'",
        "echo '{{.linelist_object}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "linelist",
          Value: "{{ .lines | splitLines | reg \"linelist_object\" }}",
          Desc: "it does not make sense that the result in local of linelist is empty\nso we do not need this var to be registered either in local or global\n",
          Expand: 0,
          Flags: {
            "vvv"
          },
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
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    dvar> linelist:
    ""
    
    [local] dvar expanded result:
    {
      "linelist": ""
    }
    
    
    scope[local] merged: {
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    
    fervent_mayer9: overall final exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
     \_ echo 'hello
    this
    is a
    beautiful world'
    hello
    this
    is a
    beautiful world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo '{{.linelist_object}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo '{{.lines}}'",
        "echo '{{.linelist}}'",
        "echo '{{.linelist_object}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "{{ .lines | splitLines | reg \"linelist_object\" }}",
          Desc: "now this var name will not be shown in local automatically\nor in global if you register it\n",
          Expand: 0,
          Flags: {
            "vvv"
          },
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      })
    })
    
    dvar> void:
    ""
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    }
    
    
    fervent_mayer9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
     \_ echo 'hello
    this
    is a
    beautiful world'
    hello
    this
    is a
    beautiful world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo '{{.linelist_object}}'
    
     \_ echo '[hello this is a beautiful world]'
    [hello this is a beautiful world]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=33) "[hello this is a beautiful world]",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "echo '{{.lines}}'",
        "echo '{{.linelist}}'",
        "echo '{{.linelist_object}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "{{ .lines | splitLines | reg \"linelist_object\" }}",
          Desc: "now this var name will not be shown in local automatically\nor in global if you register it\n",
          Expand: 0,
          Flags: {
            "vvv",
            "reg"
          },
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
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    dvar> void:
    ""
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    
    fervent_mayer9: overall final exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
     \_ echo 'hello
    this
    is a
    beautiful world'
    hello
    this
    is a
    beautiful world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo '{{.linelist_object}}'
    
     \_ echo '[hello this is a beautiful world]'
    [hello this is a beautiful world]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=33) "[hello this is a beautiful world]",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step4:
    {
      Name: "",
      Do: {
        "echo '{{.lines}}'",
        "echo '{{.linelist}}'",
        "echo '{{.linelist_object}}'"
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    
    fervent_mayer9: overall final exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
     \_ echo 'hello
    this
    is a
    beautiful world'
    hello
    this
    is a
    beautiful world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo '{{.linelist_object}}'
    
     \_ echo '[hello this is a beautiful world]'
    [hello this is a beautiful world]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=33) "[hello this is a beautiful world]",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step5:
    {
      Name: "",
      Do: <nil>,
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "person:\n  name: tom\n  age: \"18\"",
          Desc: "now this var name will not be shown in local automatically\nor in global if you register it\n",
          Expand: 0,
          Flags: {
            "vvv",
            "reg",
            "to_object"
          },
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    dvar> void:
    "person:\n  name: tom\n  age: \"18\""
    
     WARN: [?reg a void] - [you can't register a object with void name, use a proper name instead or split to multiple steps]
    dvar> void_object:
    {
      "person": {
        "age": "18",
        "name": "tom"
      }
    }
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    }
    
    
    fervent_mayer9: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
     WARN: [shell] - [Not implemented or void for no action!]
    . ok
    
```

##### Logs with different verbose level
* [c0086 log - verbose level v](../../logs/c0086_v)
* [c0086 log - verbose level vv](../../logs/c0086_vv)
* [c0086 log - verbose level vvv](../../logs/c0086_vvv)
* [c0086 log - verbose level vvvv](../../logs/c0086_vvvv)
* [c0086 log - verbose level vvvvv](../../logs/c0086_vvvvv)

##### References
* [Related Chapter](../../dvars/c0086)
