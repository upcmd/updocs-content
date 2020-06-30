---
title: "c0008_vvvvv"
date: 2020-07-01T15:34:21+77:00
draft: false
weight: 10084

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0008
                 Verbose -> vvvvv
              ModuleName -> evil_fermat0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0008
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f7be0)((len=5 cap=5) {
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
       (string) (len=1) "a": (string) (len=6) "prod-a",
       (string) (len=1) "c": (string) (len=6) "prod-c"
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
       (string) (len=1) "a": (string) (len=9) "staging-a",
       (string) (len=1) "b": (string) (len=9) "staging-b"
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
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
    
    ---------group vars----------
    
    prod: {
      "a": "prod-a",
      "c": "prod-c"
    }
    
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
    
    global: {
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    }
    
    
    groups members:[dr prod dev st staging]
    module: [evil_fermat0] instance id: [dev]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
      "c": "dev-c",
      "a": "dev-a"
    }
    
    
    merged[ dev ] runtime vars:
    {
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    }
    
    (core.Cache) (len=4) {
     (string) (len=1) "d": (string) (len=8) "global-d",
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (string) (len=5) "dev-c"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
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
      Vars: <nil>,
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
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
    }
    
    
    evil_fermat0: overall final exec vars:
    
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
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
* [c0008 log - verbose level v](../../logs/c0008_v)
* [c0008 log - verbose level vv](../../logs/c0008_vv)
* [c0008 log - verbose level vvv](../../logs/c0008_vvv)
* [c0008 log - verbose level vvvv](../../logs/c0008_vvvv)
* [c0008 log - verbose level vvvvv](../../logs/c0008_vvvvv)

##### References
* [Related Chapter](../../scope/c0008)
