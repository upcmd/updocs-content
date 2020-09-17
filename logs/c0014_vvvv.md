---
title: "c0014_vvvv"
date: 2020-09-18T00:51:21+99:00
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
    loading [Task]:  ./tests/functests/c0014
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
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e"
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
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-ref-a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 0,
      "b": "caller-ref-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "caller-ref-a",
      "e": "runtime-e",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 0,
      "b": "caller-ref-b"
    })
    
      located task-> 1 [callee_task]: 
    =Task1: [task ==> callee_task: this is ref-task ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "a": "caller-ref-a",
      "b": "caller-ref-b",
      "c": "callee-c",
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "up_runtime_task_layer_number": 1,
      "e": "runtime-e",
      "a": "caller-ref-a",
      "b": "caller-ref-b",
      "c": "callee-c"
    })
    
    cmd( 1):
    echo "exec ref-task"
    
    cmd=>:
    echo "exec ref-task"
    -
    exec ref-task
    
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
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
    """
    
    -
    
    vars:
    a: caller-ref-a
    b: caller-ref-b
    c: callee-c
    e: runtime-e
    k: runtime-k
    
    
    -
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
