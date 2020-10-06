---
title: "c0008_vvvvv"
date: 2020-10-07T00:11:02+1010:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0008
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e5cc0)((len=5 cap=5) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
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
    
    prod: (*core.Cache)({
      "a": "prod-a",
      "c": "prod-c"
    })
    
    
    nonprod: (*core.Cache)({
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    })
    
    
    global: (*core.Cache)({
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    })
    
    
    groups members:[dr prod dev st staging]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
      "a": "dev-a",
      "c": "dev-c"
    }
    
    
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a"
    })
    
    (*core.Cache)(0xc000126b00)((len=4) {
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (string) (len=5) "dev-c",
     (string) (len=1) "d": (string) (len=8) "global-d"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    })
    
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
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "non-prod-b",
      "up_runtime_task_layer_number": 0,
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a"
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
* [c0008 log - verbose level v](../../logs/c0008_v)
* [c0008 log - verbose level vv](../../logs/c0008_vv)
* [c0008 log - verbose level vvv](../../logs/c0008_vvv)
* [c0008 log - verbose level vvvv](../../logs/c0008_vvvv)
* [c0008 log - verbose level vvvvv](../../logs/c0008_vvvvv)

##### References
* [Related Chapter](../../scope/c0008)
