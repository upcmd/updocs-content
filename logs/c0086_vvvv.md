---
title: "c0086_vvvv"
date: 2020-10-07T00:11:14+1010:00
draft: false
weight: 10863

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
    loading [Task]:  ./tests/functests/c0086
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
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: generate logs ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "up_runtime_task_layer_number": 0,
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "linelist": "- hello\n- this\n- is a\n- beautiful world\n"
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
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    dvar> void:
    "- hello\n- this\n- is a\n- beautiful world\n"
    
    -
    - hello
    - this
    - is a
    - beautiful world
    
    self: final context exec vars:
    
    (*core.Cache)({
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
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
    echo '<no value>'
    -
    <no value>
    
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
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
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
    "- hello\n- this\n- is a\n- beautiful world\n"
    
    -
    - hello
    - this
    - is a
    - beautiful world
    
    self: final context exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      })
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
    echo '<no value>'
    -
    <no value>
    
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
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "lines": "hello\nthis\nis a\nbeautiful world"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
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
    cmd( 2):
    echo '{{.linelist}}'
    
    cmd=>:
    echo '<no value>'
    -
    <no value>
    
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
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      }
    })
    
    dvar> void:
    "person:\n  name: tom\n  age: \"18\""
    
    -
    person:
      name: tom
      age: "18"
     WARN: [?reg a void] - [you can't register a object with void name, use a proper name instead or split to multiple steps]
    dvar[object]> void_object:
    {
      "person": {
        "name": "tom",
        "age": "18"
      }
    }
    
    self: final context exec vars:
    
    (*core.Cache)({
      "lines": "hello\nthis\nis a\nbeautiful world",
      "linelist_object": {
        "hello",
        "this",
        "is a",
        "beautiful world"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo '[hello this is a beautiful world]'",
        Code: 0,
        Output: "[hello this is a beautiful world]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
