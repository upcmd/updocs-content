---
title: "c0085_vvvv"
date: 2020-06-25T01:55:51+66:00
draft: false
weight: 10853

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0085
                 Verbose -> vvvv
              ModuleName -> sick_hawking8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0085
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sick_hawking8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "workers": {
        "peter",
        "tom",
        "james"
      },
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
        "echo '{{.linelist}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "linelist",
          Value: "{{ .lines | splitLines }}",
          Desc: "dvar value always return a string instead of object, if you\nneed to use the object, you will need to register it to global space\n",
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
      "workers": {
        "peter",
        "tom",
        "james"
      }
    })
    
    dvar> linelist:
    "[hello this is a beautiful world]"
    
    sick_hawking8: overall final exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist": "[hello this is a beautiful world]",
      "workers": {
        "peter",
        "tom",
        "james"
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
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '[hello this is a beautiful world]'
    [hello this is a beautiful world]
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "echo '{{.lines}}'",
        "echo '{{.linelist}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "linelist",
          Value: "{{ .lines | splitLines | printobj }}",
          Desc: "",
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
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    {
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    dvar> linelist:
    "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n"
    
    sick_hawking8: overall final exec vars:
    
    (*core.Cache)({
      "linelist": "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n",
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "workers": {
        "peter",
        "tom",
        "james"
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
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '{
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    '
    {
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
     .. ok
    . ok
    -Step3: [regtest:  ]
    {
      Name: "regtest",
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
          Desc: "",
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
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      })
    })
    
    dvar> linelist:
    ""
    
    sick_hawking8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      }),
      "workers": {
        "peter",
        "tom",
        "james"
      },
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
    cmd( 2):
    echo '{{.linelist}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    cmd( 3):
    echo '{{.linelist_object}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    . ok
    -Step4:
    {
      Name: "",
      Do: {
        "echo \"{{.loopindex1}} -> {{.loopitem}}\""
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
      Loop: "workers",
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      })
    })
    
    sick_hawking8: overall final exec vars:
    
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "1 -> peter"
    1 -> peter
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "2 -> tom"
    2 -> tom
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "3 -> james"
    3 -> james
     .. ok
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        "echo \"{{.loopindex1}} -> {{.loopitem}}\""
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
      Loop: "linelist_object",
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "3 -> james",
        ErrMsg: ""
      }),
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    sick_hawking8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "3 -> james",
        ErrMsg: ""
      }),
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "1 -> hello"
    1 -> hello
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "2 -> this"
    2 -> this
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "3 -> is a"
    3 -> is a
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
     \_ echo "4 -> beautiful world"
    4 -> beautiful world
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0085 log - verbose level v](../../logs/c0085_v)
* [c0085 log - verbose level vv](../../logs/c0085_vv)
* [c0085 log - verbose level vvv](../../logs/c0085_vvv)
* [c0085 log - verbose level vvvv](../../logs/c0085_vvvv)
* [c0085 log - verbose level vvvvv](../../logs/c0085_vvvvv)

##### References
* [Related Chapter](../../template/c0085)
