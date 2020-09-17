---
title: "c0017_vvvv"
date: 2020-09-18T00:51:21+99:00
draft: false
weight: 10173

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0017
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0017
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
      located task-> 2 [task]: 
    Task2: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: call1 ]
    current exec runtime vars:
    (*core.Cache)({
      "k": "runtime-k",
      "a": "caller-ref-1a",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 0,
      "b": "caller-ref-1b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "b": "caller-ref-1b",
      "k": "runtime-k",
      "a": "caller-ref-1a",
      "e": "runtime-e"
    })
    
      located task-> 1 [callee_task1]: 
    =Task1: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "callee-c",
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1,
      "k": "runtime-k"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "k": "runtime-k",
      "c": "callee-c",
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "e": "runtime-e"
    })
    
    cmd( 1):
    echo "exec ref-task1"
    
    cmd=>:
    echo "exec ref-task1"
    -
    exec ref-task1
    
    -
     .. ok
    cmd( 2):
    echo """
    vars:
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    e: {{.e}}
    k: {{.k}}
    """
    
    
    cmd=>:
    echo """
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    -
    
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    
    
    -
     .. ok
    . ok
      located task-> 3 [callee_task2]: 
    =Task3: [task ==> callee_task2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nvars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k\n\"\"\"\n",
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nvars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k\n\"\"\"\n",
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "k": "runtime-k",
      "e": "runtime-e"
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
    cmd=>:
    echo "exec ref-task2"
    -
    exec ref-task2
    
    -
     .. ok
    cmd( 2):
    echo """
    vars:
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    e: {{.e}}
    k: {{.k}}
    """
    
    
    cmd=>:
    echo """
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    -
    
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    
    
    -
     .. ok
    . ok
    -Step2: [: call2 ]
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "a": "caller-ref-2a",
      "e": "runtime-e"
    })
    
      located task-> 3 [callee_task2]: 
    =Task3: [task ==> callee_task2:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "callee-c",
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "caller-ref-2b",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "k": "runtime-k",
      "c": "callee-c",
      "a": "caller-ref-2a"
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
    cmd=>:
    echo "exec ref-task2"
    -
    exec ref-task2
    
    -
     .. ok
    cmd( 2):
    echo """
    vars:
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    e: {{.e}}
    k: {{.k}}
    """
    
    
    cmd=>:
    echo """
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    -
    
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    
    
    -
     .. ok
    . ok
      located task-> 1 [callee_task1]: 
    =Task1: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "c": "callee-c",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nvars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k\n\"\"\"\n",
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "c": "callee-c",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"\"\"\nvars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k\n\"\"\"\n",
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    cmd( 1):
    echo "exec ref-task1"
    
    cmd=>:
    echo "exec ref-task1"
    -
    exec ref-task1
    
    -
     .. ok
    cmd( 2):
    echo """
    vars:
    a: {{.a}}
    b: {{.b}}
    c: {{.c}}
    e: {{.e}}
    k: {{.k}}
    """
    
    
    cmd=>:
    echo """
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    -
    
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0017 log - verbose level v](../../logs/c0017_v)
* [c0017 log - verbose level vv](../../logs/c0017_vv)
* [c0017 log - verbose level vvv](../../logs/c0017_vvv)
* [c0017 log - verbose level vvvv](../../logs/c0017_vvvv)
* [c0017 log - verbose level vvvvv](../../logs/c0017_vvvvv)

##### References
* [Related Chapter](../../call-func/c0017)
