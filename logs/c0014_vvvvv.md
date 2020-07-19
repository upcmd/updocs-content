---
title: "c0014_vvvvv"
date: 2020-07-20T02:01:31+77:00
draft: false
weight: 10144

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0014
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0014
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175060)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "a": (string) (len=9) "runtime-a",
     (string) (len=1) "e": (string) (len=9) "runtime-e",
     (string) (len=1) "k": (string) (len=9) "runtime-k"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e"
    }
    
      located task-> 2 [task]: 
    Task2: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "callee_task"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "caller-ref-a",
        "b": "caller-ref-b"
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
      "b": "caller-ref-b",
      "k": "runtime-k",
      "a": "caller-ref-a",
      "e": "runtime-e"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "k": "runtime-k",
      "a": "caller-ref-a",
      "e": "runtime-e",
      "b": "caller-ref-b"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-a",
      "e": "runtime-e",
      "b": "caller-ref-b",
      "k": "runtime-k"
    })
    
    caller's vars to task (callee_task)::
    (*core.Cache)({
      "k": "runtime-k",
      "a": "caller-ref-a",
      "e": "runtime-e",
      "b": "caller-ref-b"
    })
    
      located task-> 1 [callee_task]: 
    =Task1: [task ==> callee_task: this is ref-task ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"exec ref-task\"",
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
      "a": "caller-ref-a",
      "b": "caller-ref-b",
      "c": "callee-c",
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "caller-ref-a",
      "b": "caller-ref-b",
      "c": "callee-c",
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-a",
      "b": "caller-ref-b",
      "c": "callee-c",
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "exec ref-task"
    
    cmd=>:
    echo "exec ref-task"<=
    exec ref-task
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \"exec ref-task\"",
     Code: (int) 0,
     Output: (string) (len=13) "exec ref-task",
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
    
    
    cmd=>:
    echo """
    vars:
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    <=
    vars:
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=89) "echo \"\"\"\nvars:\na: caller-ref-a\nb: caller-ref-b\nc: callee-c\ne: runtime-e\nk: runtime-k\n\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=75) "vars:\na: caller-ref-a\nb: caller-ref-b\nc: callee-c\ne: runtime-e\nk: runtime-k",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0014 log - verbose level v](../../logs/c0014_v)
* [c0014 log - verbose level vv](../../logs/c0014_vv)
* [c0014 log - verbose level vvv](../../logs/c0014_vvv)
* [c0014 log - verbose level vvvv](../../logs/c0014_vvvv)
* [c0014 log - verbose level vvvvv](../../logs/c0014_vvvvv)

##### References
* [Related Chapter](../../vars/c0014)
