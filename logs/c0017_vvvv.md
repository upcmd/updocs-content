---
title: "c0017_vvvv"
date: 2020-07-01T15:34:22+77:00
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
              ModuleName -> hopeful_poitras8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0017
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hopeful_poitras8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
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
    {
      Name: "",
      Do: {
        "callee_task1",
        "callee_task2"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "caller-ref-1a",
        "b": "caller-ref-1b"
      },
      Dvars: <nil>,
      Desc: "call1",
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
      "a": "caller-ref-1a",
      "e": "runtime-e",
      "k": "runtime-k",
      "b": "caller-ref-1b"
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "b": "caller-ref-1b",
      "a": "caller-ref-1a",
      "e": "runtime-e"
    })
    
      located task-> 1 [callee_task1]: 
    =Task1: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"exec ref-task1\"",
        "echo \"\"\"\nvars:\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\ne: {{.e}}\nk: {{.k}}\n\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "b": "callee-b",
        "c": "callee-c",
        "a": "callee-a"
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
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "c": "callee-c",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-1a",
      "b": "caller-ref-1b"
    })
    
    cmd( 1):
    echo "exec ref-task1"
    
     \_ echo "exec ref-task1"
    exec ref-task1
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
    
    
     \_ echo """
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
     .. ok
    . ok
      located task-> 3 [callee_task2]: 
    =Task3: [task ==> callee_task2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"exec ref-task2\"",
        "echo \"\"\"\nvars:\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\ne: {{.e}}\nk: {{.k}}\n\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "callee-a",
        "b": "callee-b",
        "c": "callee-c"
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
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "b": "caller-ref-1b",
      "c": "callee-c",
      "a": "caller-ref-1a"
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "b": "caller-ref-1b",
      "c": "callee-c",
      "a": "caller-ref-1a",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
     \_ echo "exec ref-task2"
    exec ref-task2
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
    
    
     \_ echo """
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    vars:
    a: caller-ref-1a
    b: caller-ref-1b
    c: callee-c
    e: runtime-e
    k: runtime-k
     .. ok
    . ok
    -Step2: [: call2 ]
    {
      Name: "",
      Do: {
        "callee_task2",
        "callee_task1"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "caller-ref-2a",
        "b": "caller-ref-2b"
      },
      Dvars: <nil>,
      Desc: "call2",
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
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b"
    })
    
      located task-> 3 [callee_task2]: 
    =Task3: [task ==> callee_task2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"exec ref-task2\"",
        "echo \"\"\"\nvars:\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\ne: {{.e}}\nk: {{.k}}\n\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "callee-a",
        "b": "callee-b",
        "c": "callee-c"
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
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "c": "callee-c",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e"
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "c": "callee-c",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e"
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
     \_ echo "exec ref-task2"
    exec ref-task2
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
    
    
     \_ echo """
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
     .. ok
    . ok
      located task-> 1 [callee_task1]: 
    =Task1: [task ==> callee_task1:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"exec ref-task1\"",
        "echo \"\"\"\nvars:\na: {{.a}}\nb: {{.b}}\nc: {{.c}}\ne: {{.e}}\nk: {{.k}}\n\"\"\"\n"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "b": "callee-b",
        "c": "callee-c",
        "a": "callee-a"
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
      "b": "caller-ref-2b",
      "c": "callee-c",
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      })
    })
    
    hopeful_poitras8: overall final exec vars:
    
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "b": "caller-ref-2b",
      "c": "callee-c",
      "a": "caller-ref-2a"
    })
    
    cmd( 1):
    echo "exec ref-task1"
    
     \_ echo "exec ref-task1"
    exec ref-task1
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
    
    
     \_ echo """
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    vars:
    a: caller-ref-2a
    b: caller-ref-2b
    c: callee-c
    e: runtime-e
    k: runtime-k
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
