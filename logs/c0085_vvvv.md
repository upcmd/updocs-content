---
title: "c0085_vvvv"
date: 2020-10-07T00:11:14+1010:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0085
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0,
      "workers": {
        "peter",
        "tom",
        "james"
      }
    })
    
    dvar> linelist:
    "[hello this is a beautiful world]"
    
    -
    [hello this is a beautiful world]
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
    cmd( 2):
    echo '{{.linelist}}'
    
    cmd=>:
    echo '[hello this is a beautiful world]'
    -
    [hello this is a beautiful world]
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world"
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
    . ok
    -Step3: [regtest:  ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
        Code: 0,
        Output: "{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}",
        ErrMsg: ""
      }),
      "workers": {
        "peter",
        "tom",
        "james"
      },
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0
    })
    
    dvar> linelist:
    "- hello\n- this\n- is a\n- beautiful world\n"
    
    -
    - hello
    - this
    - is a
    - beautiful world
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "linelist": "- hello\n- this\n- is a\n- beautiful world\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '{\n  \"hello\",\n  \"this\",\n  \"is a\",\n  \"beautiful world\"\n}\n\n'",
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
    cmd( 3):
    echo '{{.linelist_object}}'
    
    cmd=>:
    echo '[hello this is a beautiful world]'
    -
    [hello this is a beautiful world]
    
    -
     .. ok
    . ok
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "1 -> peter"
    -
    1 -> peter
    
    -
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "2 -> tom"
    -
    2 -> tom
    
    -
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "3 -> james"
    -
    3 -> james
    
    -
     .. ok
    . ok
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
        Cmd: "echo \"3 -> james\"",
        Code: 0,
        Output: "3 -> james",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
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
        Cmd: "echo \"3 -> james\"",
        Code: 0,
        Output: "3 -> james",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "1 -> hello"
    -
    1 -> hello
    
    -
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "2 -> this"
    -
    2 -> this
    
    -
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "3 -> is a"
    -
    3 -> is a
    
    -
     .. ok
    cmd( 1):
    echo "{{.loopindex1}} -> {{.loopitem}}"
    
    cmd=>:
    echo "4 -> beautiful world"
    -
    4 -> beautiful world
    
    -
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
