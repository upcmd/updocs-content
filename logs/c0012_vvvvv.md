---
title: "c0012_vvvvv"
date: 2020-09-18T01:27:22+99:00
draft: false
weight: 10124

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0012
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
    loading [Task]:  ./tests/functests/c0012
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bef60)(<nil>)
    
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
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: to test display env vars from shell context ]
    {
      Name: "",
      Do: {
        "echo \"hello, world\"",
        "echo 'hello {{.a}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "to test display env vars from shell context",
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
      "up_runtime_task_layer_number": 0,
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "k": "runtime-k",
      "a": "runtime-a",
      "e": "runtime-e",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "hello, world"
    
    cmd=>:
    echo "hello, world"
    -
    hello, world
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"hello, world\"",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo 'hello {{.a}}'
    
    cmd=>:
    echo 'hello runtime-a'
    -
    hello runtime-a
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo 'hello runtime-a'",
     Code: (int) 0,
     Output: (string) (len=15) "hello runtime-a",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0012 log - verbose level v](../../logs/c0012_v)
* [c0012 log - verbose level vv](../../logs/c0012_vv)
* [c0012 log - verbose level vvv](../../logs/c0012_vvv)
* [c0012 log - verbose level vvvv](../../logs/c0012_vvvv)
* [c0012 log - verbose level vvvvv](../../logs/c0012_vvvvv)

##### References
* [Related Chapter](../../vars/c0012)
