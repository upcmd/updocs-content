---
title: "c0012_vvvvv"
date: 2020-06-27T03:09:15+66:00
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
              ModuleName -> mad_yalow6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0012
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eee80)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [mad_yalow6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
    }
    
    (core.Cache) (len=3) {
     (string) (len=1) "k": (string) (len=9) "runtime-k",
     (string) (len=1) "a": (string) (len=9) "runtime-a",
     (string) (len=1) "e": (string) (len=9) "runtime-e"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    
    mad_yalow6: overall final exec vars:
    
    (*core.Cache)({
      "e": "runtime-e",
      "k": "runtime-k",
      "a": "runtime-a"
    })
    
    cmd( 1):
    echo "hello, world"
    
     \_ echo "hello, world"
    hello, world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo 'hello {{.a}}'
    
     \_ echo 'hello runtime-a'
    hello runtime-a
     .. ok
    (utils.ExecResult) {
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
