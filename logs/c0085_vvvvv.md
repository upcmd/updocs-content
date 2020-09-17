---
title: "c0085_vvvvv"
date: 2020-09-18T01:27:34+99:00
draft: false
weight: 10854

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
    loading [Task]:  ./tests/functests/c0085
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175620)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
    }
    
    (core.Cache) (len=2) {
     (string) (len=7) "workers": ([]interface {}) (len=3 cap=3) {
      (string) (len=5) "peter",
      (string) (len=3) "tom",
      (string) (len=5) "james"
     },
     (string) (len=5) "lines": (string) (len=31) "hello\nthis\nis a\nbeautiful world"
    }
    
    [runtime global] dvar expanded result:
    {
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0
    })
    
    dvar> linelist:
    "[hello this is a beautiful world]"
    
    -
    [hello this is a beautiful world]
    [local] dvar expanded result:
    {
      "linelist": "[hello this is a beautiful world]"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist": "[hello this is a beautiful world]"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0,
      "linelist": "[hello this is a beautiful world]"
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
    cmd=>:
    echo 'hello
    this
    is a
    beautiful world'
    -
    hello
    this
    is a
    beautiful world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=38) "echo 'hello\nthis\nis a\nbeautiful world'",
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
    cmd=>:
    echo '[hello this is a beautiful world]'
    -
    [hello this is a beautiful world]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=40) "echo '[hello this is a beautiful world]'",
     Code: (int) 0,
     Output: (string) (len=33) "[hello this is a beautiful world]",
     ErrMsg: (string) ""
    }
    
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
          Value: "{{ .lines | splitLines | printObj }}",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    {
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    dvar> linelist:
    "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n"
    
    -
    {
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    
    [local] dvar expanded result:
    {
      "linelist": "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n"
    }
    
    
    scope[local] merged: {
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "linelist": "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "linelist": "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n"
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
    cmd=>:
    echo 'hello
    this
    is a
    beautiful world'
    -
    hello
    this
    is a
    beautiful world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=38) "echo 'hello\nthis\nis a\nbeautiful world'",
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
    cmd=>:
    echo '{
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    '
    -
    {
      "hello",
      "this",
      "is a",
      "beautiful world"
    }
    
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=63) "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
     Code: (int) 0,
     Output: (string) (len=54) "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    dvar> linelist:
    "- hello\n- this\n- is a\n- beautiful world\n"
    
    -
    - hello
    - this
    - is a
    - beautiful world
    
    [local] dvar expanded result:
    {
      "linelist": "- hello\n- this\n- is a\n- beautiful world\n",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    }
    
    
    scope[local] merged: {
      "linelist": "- hello\n- this\n- is a\n- beautiful world\n",
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "linelist": "- hello\n- this\n- is a\n- beautiful world\n",
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo '{{.lines}}'
    
    cmd=>:
    echo 'hello
    this
    is a
    beautiful world'
    -
    hello
    this
    is a
    beautiful world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=38) "echo 'hello\nthis\nis a\nbeautiful world'",
     Code: (int) 0,
     Output: (string) (len=31) "hello\nthis\nis a\nbeautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo '{{.linelist}}'
    
    cmd=>:
    echo '- hello
    - this
    - is a
    - beautiful world
    '
    -
    - hello
    - this
    - is a
    - beautiful world
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=47) "echo '- hello\n- this\n- is a\n- beautiful world\n'",
     Code: (int) 0,
     Output: (string) (len=39) "- hello\n- this\n- is a\n- beautiful world",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo '{{.linelist_object}}'
    
    cmd=>:
    echo '[hello this is a beautiful world]'
    -
    [hello this is a beautiful world]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=40) "echo '[hello this is a beautiful world]'",
     Code: (int) 0,
     Output: (string) (len=33) "[hello this is a beautiful world]",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0
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
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
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
      }
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "1 -> peter"
    -
    1 -> peter
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"1 -> peter\"",
     Code: (int) 0,
     Output: (string) (len=10) "1 -> peter",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "2 -> tom"
    -
    2 -> tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=15) "echo \"2 -> tom\"",
     Code: (int) 0,
     Output: (string) (len=8) "2 -> tom",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "3 -> james"
    -
    3 -> james
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"3 -> james\"",
     Code: (int) 0,
     Output: (string) (len=10) "3 -> james",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"3 -> james\"",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "lines": "hello\nthis\nis a\nbeautiful world",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"3 -> james\"",
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
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"3 -> james\"",
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
      "up_runtime_task_layer_number": 0,
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "1 -> hello"
    -
    1 -> hello
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"1 -> hello\"",
     Code: (int) 0,
     Output: (string) (len=10) "1 -> hello",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "2 -> this"
    -
    2 -> this
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"2 -> this\"",
     Code: (int) 0,
     Output: (string) (len=9) "2 -> this",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "3 -> is a"
    -
    3 -> is a
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "echo \"3 -> is a\"",
     Code: (int) 0,
     Output: (string) (len=9) "3 -> is a",
     ErrMsg: (string) ""
    }
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "4 -> beautiful world"
    -
    4 -> beautiful world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"4 -> beautiful world\"",
     Code: (int) 0,
     Output: (string) (len=20) "4 -> beautiful world",
     ErrMsg: (string) ""
    }
    
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
