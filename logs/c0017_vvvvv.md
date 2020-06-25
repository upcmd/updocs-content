---
title: "c0017_vvvvv"
date: 2020-06-25T01:55:39+66:00
draft: false
weight: 10174

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
                 Verbose -> vvvvv
              ModuleName -> admiring_brattain1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0017
    -------full vars in scopes------
    (*impl.Scopes)(0xc00026d2c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [admiring_brattain1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "e": (string) (len=9) "runtime-e",
     (string) (len=1) "k": (string) (len=9) "runtime-k",
     (string) (len=1) "a": (string) (len=9) "runtime-a"
    }
    
    [runtime global] dvar expanded result:
    {
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
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "caller-ref-1a",
      "b": "caller-ref-1b"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    caller's vars to task (callee_task1)::
    (*core.Cache)({
      "k": "runtime-k",
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
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
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c",
      "e": "runtime-e"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "exec ref-task1",
     ErrMsg: (string) ""
    }
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=77) "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (callee_task2)::
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "a": "caller-ref-1a",
      "b": "caller-ref-1b"
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
        "c": "callee-c",
        "a": "callee-a",
        "b": "callee-b"
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
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "k": "runtime-k",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "caller-ref-1b",
      "c": "callee-c",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "k": "runtime-k",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "a": "caller-ref-1a"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "k": "runtime-k",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "a": "caller-ref-1a",
      "b": "caller-ref-1b",
      "c": "callee-c"
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
     \_ echo "exec ref-task2"
    exec ref-task2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "exec ref-task2",
     ErrMsg: (string) ""
    }
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=77) "vars:\na: caller-ref-1a\nb: caller-ref-1b\nc: callee-c\ne: runtime-e\nk: runtime-k",
     ErrMsg: (string) ""
    }
    
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
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "a": "caller-ref-2a"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    caller's vars to task (callee_task2)::
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "a": "caller-ref-2a"
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
      "c": "callee-c",
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "c": "callee-c",
      "a": "caller-ref-2a",
      "b": "caller-ref-2b"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "c": "callee-c",
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "e": "runtime-e",
      "k": "runtime-k"
    })
    
    cmd( 1):
    echo "exec ref-task2"
    
     \_ echo "exec ref-task2"
    exec ref-task2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "exec ref-task2",
     ErrMsg: (string) ""
    }
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=77) "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (callee_task1)::
    (*core.Cache)({
      "a": "caller-ref-2a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "b": "caller-ref-2b",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      })
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
      "b": "caller-ref-2b",
      "c": "callee-c",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-2a"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "caller-ref-2b",
      "c": "callee-c",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-2a"
    }
    
    
    admiring_brattain1: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
        ErrMsg: ""
      }),
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "a": "caller-ref-2a",
      "b": "caller-ref-2b",
      "c": "callee-c"
    })
    
    cmd( 1):
    echo "exec ref-task1"
    
     \_ echo "exec ref-task1"
    exec ref-task1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "exec ref-task1",
     ErrMsg: (string) ""
    }
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=77) "vars:\na: caller-ref-2a\nb: caller-ref-2b\nc: callee-c\ne: runtime-e\nk: runtime-k",
     ErrMsg: (string) ""
    }
    
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