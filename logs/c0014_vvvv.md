---
title: "c0014_vvvv"
date: 2020-06-27T03:09:15+66:00
draft: false
weight: 10143

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
                 Verbose -> vvvv
              ModuleName -> gloomy_hypatia4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0014
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [gloomy_hypatia4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
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
    
    gloomy_hypatia4: overall final exec vars:
    
    (*core.Cache)({
      "b": "caller-ref-b",
      "k": "runtime-k",
      "a": "caller-ref-a",
      "e": "runtime-e"
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
      "b": "caller-ref-b",
      "c": "callee-c",
      "a": "caller-ref-a",
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1
    })
    
    gloomy_hypatia4: overall final exec vars:
    
    (*core.Cache)({
      "b": "caller-ref-b",
      "c": "callee-c",
      "a": "caller-ref-a",
      "k": "runtime-k",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "exec ref-task"
    
     \_ echo "exec ref-task"
    exec ref-task
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
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    vars:
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
     .. ok
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
