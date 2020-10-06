---
title: "c0010_vvvvv"
date: 2020-10-07T00:11:02+1010:00
draft: false
weight: 10104

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0010
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
    loading [Task]:  ./tests/functests/c0010
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000173300)((len=5 cap=5) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "d": (string) (len=8) "global-d",
       (string) (len=1) "a": (string) (len=8) "global-a",
       (string) (len=1) "b": (string) (len=8) "global-b",
       (string) (len=1) "c": (map[interface {}]interface {}) (len=4) {
        (string) (len=2) "c1": (string) (len=9) "global-c1",
        (string) (len=2) "c2": (string) (len=9) "global-c2",
        (string) (len=2) "c3": (map[interface {}]interface {}) (len=3) {
         (string) (len=3) "c32": (string) (len=10) "global-c32",
         (string) (len=3) "c33": (string) (len=10) "global-c33",
         (string) (len=3) "c31": (string) (len=10) "global-c31"
        },
        (string) (len=2) "c4": (string) (len=9) "global-c4"
       }
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
       (string) (len=1) "c": (map[interface {}]interface {}) (len=5) {
        (string) (len=2) "c1": (string) (len=10) "nonprod-c1",
        (string) (len=2) "c2": (string) (len=10) "nonprod-c2",
        (string) (len=2) "c3": (map[interface {}]interface {}) (len=2) {
         (string) (len=3) "c32": (string) (len=11) "nonprod-c32",
         (string) (len=3) "c33": (string) (len=11) "nonprod-c33"
        },
        (string) (len=2) "c4": (string) (len=10) "nonprod-c4",
        (string) (len=2) "c5": (string) (len=10) "nonprod-c5"
       }
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
       (string) (len=1) "c": (map[interface {}]interface {}) (len=5) {
        (string) (len=2) "c1": (string) (len=6) "dev-c1",
        (string) (len=2) "c2": (string) (len=6) "dev-c2",
        (string) (len=2) "c3": (map[interface {}]interface {}) (len=1) {
         (string) (len=3) "c33": (string) (len=7) "dev-c33"
        },
        (string) (len=2) "c6": (string) (len=6) "dev-c6",
        (string) (len=2) "c7": (string) (len=6) "dev-c7"
       }
      },
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [global] dvar expanded result:
    {
    }
    
    
    scope[global] merged: {
      "a": "global-a",
      "b": "global-b",
      "c": {
        "c1": "global-c1",
        "c2": "global-c2",
        "c3": {
          "c31": "global-c31",
          "c32": "global-c32",
          "c33": "global-c33"
        },
        "c4": "global-c4"
      },
      "d": "global-d"
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
      "c": {
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c1": "nonprod-c1",
        "c2": "nonprod-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "nonprod-c33"
        }
      }
    }
    
    
    ---------group vars----------
    
    prod: (*core.Cache)({
      "c": "prod-c",
      "a": "prod-a"
    })
    
    
    nonprod: (*core.Cache)({
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": {
        "c5": "nonprod-c5",
        "c1": "nonprod-c1",
        "c2": "nonprod-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "nonprod-c33"
        },
        "c4": "nonprod-c4"
      }
    })
    
    
    global: (*core.Cache)({
      "b": "global-b",
      "c": {
        "c1": "global-c1",
        "c2": "global-c2",
        "c3": {
          "c33": "global-c33",
          "c31": "global-c31",
          "c32": "global-c32"
        },
        "c4": "global-c4"
      },
      "d": "global-d",
      "a": "global-a"
    })
    
    
    groups members:[dr prod dev st staging]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
      "a": "dev-a",
      "c": {
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c1": "dev-c1",
        "c2": "dev-c2",
        "c3": {
          "c33": "dev-c33"
        }
      }
    }
    
    
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c4": "nonprod-c4",
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c31": "global-c31",
          "c32": "nonprod-c32",
          "c33": "dev-c33"
        }
      }
    })
    
    (*core.Cache)(0xc0000b6ad8)((len=4) {
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (map[interface {}]interface {}) (len=7) {
      (string) (len=2) "c3": (map[interface {}]interface {}) (len=3) {
       (string) (len=3) "c33": (string) (len=7) "dev-c33",
       (string) (len=3) "c31": (string) (len=10) "global-c31",
       (string) (len=3) "c32": (string) (len=11) "nonprod-c32"
      },
      (string) (len=2) "c4": (string) (len=10) "nonprod-c4",
      (string) (len=2) "c1": (string) (len=6) "dev-c1",
      (string) (len=2) "c5": (string) (len=10) "nonprod-c5",
      (string) (len=2) "c6": (string) (len=6) "dev-c6",
      (string) (len=2) "c7": (string) (len=6) "dev-c7",
      (string) (len=2) "c2": (string) (len=6) "dev-c2"
     },
     (string) (len=1) "d": (string) (len=8) "global-d"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c4": "nonprod-c4",
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        }
      },
      "d": "global-d"
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
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c4": "nonprod-c4",
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        }
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "non-prod-b",
      "c": {
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c33": "dev-c33",
          "c31": "global-c31",
          "c32": "nonprod-c32"
        },
        "c4": "nonprod-c4",
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6"
      },
      "up_runtime_task_layer_number": 0,
      "d": "global-d",
      "a": "dev-a"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "d": "global-d",
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        },
        "c4": "nonprod-c4",
        "c1": "dev-c1"
      }
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
* [c0010 log - verbose level v](../../logs/c0010_v)
* [c0010 log - verbose level vv](../../logs/c0010_vv)
* [c0010 log - verbose level vvv](../../logs/c0010_vvv)
* [c0010 log - verbose level vvvv](../../logs/c0010_vvvv)
* [c0010 log - verbose level vvvvv](../../logs/c0010_vvvvv)

##### References
* [Related Chapter](../../scope/c0010)
