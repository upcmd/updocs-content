---
title: "c0009_vvvvv"
date: 2020-08-18T15:15:48+88:00
draft: false
weight: 10094

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0009
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0009
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    loading [ref vars]:  ./tests/functests/d0009-global.yml
    (core.Cache) (len=4) {
     (string) (len=1) "d": (string) (len=8) "global-d",
     (string) (len=1) "a": (string) (len=8) "global-a",
     (string) (len=1) "b": (string) (len=8) "global-b",
     (string) (len=1) "c": (string) (len=8) "global-c"
    }
    
    loading vars from: d0009-global.yml
    
    {
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    }
    
    loading [ref vars]:  ./tests/functests/d0009-dev.yml
    (core.Cache) (len=2) {
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=1) "c": (string) (len=5) "dev-c"
    }
    
    loading vars from: d0009-dev.yml
    
    {
      "a": "dev-a",
      "c": "dev-c"
    }
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00023f200)((len=5 cap=5) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) (len=16) "d0009-global.yml",
      RefDir: (string) (len=17) "./tests/functests",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "b": (string) (len=8) "global-b",
       (string) (len=1) "c": (string) (len=8) "global-c",
       (string) (len=1) "d": (string) (len=8) "global-d",
       (string) (len=1) "a": (string) (len=8) "global-a"
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
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c",
       (string) (len=1) "a": (string) (len=10) "non-prod-a"
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
      Ref: (string) (len=13) "d0009-dev.yml",
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
      "d": "global-d",
      "a": "global-a",
      "b": "global-b",
      "c": "global-c"
    }
    
    
    [prod] dvar expanded result:
    {
    }
    
    
    scope[prod] merged: {
      "c": "prod-c",
      "a": "prod-a"
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
    
    
    prod: {
      "a": "prod-a",
      "c": "prod-c"
    }
    
    
    groups members:[dr prod dev st staging]
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
      "a": "dev-a",
      "b": "non-prod-b"
    }
    
    (core.Cache) (len=4) {
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (string) (len=5) "dev-c",
     (string) (len=1) "d": (string) (len=8) "global-d",
     (string) (len=1) "a": (string) (len=5) "dev-a"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    })
    
    cmd( 1):
    echo "test out the var scopes only"
    
    cmd=>:
    echo "test out the var scopes only"
    -
    test out the var scopes only
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=35) "echo \"test out the var scopes only\"",
     Code: (int) 0,
     Output: (string) (len=28) "test out the var scopes only",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0009 log - verbose level v](../../logs/c0009_v)
* [c0009 log - verbose level vv](../../logs/c0009_vv)
* [c0009 log - verbose level vvv](../../logs/c0009_vvv)
* [c0009 log - verbose level vvvv](../../logs/c0009_vvvv)
* [c0009 log - verbose level vvvvv](../../logs/c0009_vvvvv)

##### References
* [Related Chapter](../../scope/c0009)
