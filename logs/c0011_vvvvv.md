---
title: "c0011_vvvvv"
date: 2020-06-25T01:55:38+66:00
draft: false
weight: 10114

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0011
                 Verbose -> vvvvv
              ModuleName -> determined_jang7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0011
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef1e0)((len=5 cap=5) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "a": (string) (len=8) "global-a",
       (string) (len=1) "b": (string) (len=8) "global-b",
       (string) (len=1) "c": (string) (len=8) "global-c",
       (string) (len=1) "d": (string) (len=8) "global-d"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=4) "prod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=2) "dr",
       (string) (len=4) "prod"
      },
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "c": (string) (len=6) "prod-c",
       (string) (len=1) "a": (string) (len=6) "prod-a"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=3 cap=3) {
       (string) (len=3) "dev",
       (string) (len=2) "st",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=3) {
       (string) (len=1) "a": (string) (len=10) "non-prod-a",
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=7) "staging",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "b": (string) (len=9) "staging-b",
       (string) (len=1) "a": (string) (len=9) "staging-a"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=3) "dev",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "a": (string) (len=5) "dev-a",
       (string) (len=1) "c": (string) (len=5) "dev-c"
      },
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [global] dvar expanded result:
    {
    }
    
    
    scope[global] merged: {
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    }
    
    
    [prod] dvar expanded result:
    {
    }
    
    
    scope[prod] merged: {
      "a": "prod-a",
      "c": "prod-c"
    }
    
    
    [nonprod] dvar expanded result:
    {
    }
    
    
    scope[nonprod] merged: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "a": "non-prod-a"
    }
    
    
    ---------group vars----------
    
    prod: {
      "c": "prod-c",
      "a": "prod-a"
    }
    
    
    nonprod: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "a": "non-prod-a"
    }
    
    
    global: {
      "c": "global-c",
      "d": "global-d",
      "a": "global-a",
      "b": "global-b"
    }
    
    
    groups members:[dr prod dev st staging]
    module: [determined_jang7] instance id: [dev]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
      "a": "dev-a",
      "c": "dev-c"
    }
    
    
    merged[ dev ] runtime vars:
    {
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "b": "non-prod-b",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
    (core.Cache) (len=6) {
     (string) (len=1) "d": (string) (len=8) "global-d",
     (string) (len=1) "a": (string) (len=9) "runtime-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "e": (string) (len=9) "runtime-e",
     (string) (len=1) "k": (string) (len=9) "runtime-k",
     (string) (len=1) "c": (string) (len=5) "dev-c"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "b": "non-prod-b",
      "e": "runtime-e",
      "k": "runtime-k"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"test out the var scopes only\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "e": "local-e",
        "m": "local-m"
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
      "b": "non-prod-b",
      "e": "local-e",
      "k": "runtime-k",
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "m": "local-m"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "m": "local-m",
      "b": "non-prod-b",
      "e": "local-e",
      "k": "runtime-k"
    }
    
    
    determined_jang7: overall final exec vars:
    
    (*core.Cache)({
      "b": "non-prod-b",
      "e": "local-e",
      "k": "runtime-k",
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "m": "local-m"
    })
    
    cmd( 1):
    echo "test out the var scopes only"
    
     \_ echo "test out the var scopes only"
    test out the var scopes only
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=28) "test out the var scopes only",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0011 log - verbose level v](../../logs/c0011_v)
* [c0011 log - verbose level vv](../../logs/c0011_vv)
* [c0011 log - verbose level vvv](../../logs/c0011_vvv)
* [c0011 log - verbose level vvvv](../../logs/c0011_vvvv)
* [c0011 log - verbose level vvvvv](../../logs/c0011_vvvvv)

##### References
* [Related Chapter](../../scope/c0011)