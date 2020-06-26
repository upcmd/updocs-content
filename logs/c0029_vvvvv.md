---
title: "c0029_vvvvv"
date: 2020-06-27T03:09:17+66:00
draft: false
weight: 10294

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0029
                 Verbose -> vvvvv
              ModuleName -> grave_pike6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0029
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb280)((len=3 cap=3) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "a": (string) (len=8) "global-a",
       (string) (len=1) "b": (string) (len=8) "global-b",
       (string) (len=1) "c": (string) (len=8) "global-c",
       (string) (len=1) "e": (string) (len=8) "global-e"
      },
      Dvars: (impl.Dvars) (len=2 cap=2) {
       (impl.Dvar) {
        Name: (string) (len=2) "da",
        Value: (string) (len=6) "{{.a}}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       },
       (impl.Dvar) {
        Name: (string) (len=3) "dab",
        Value: (string) (len=17) "{{.a}}-and-{{.b}}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=3) "dev",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c",
       (string) (len=1) "d": (string) (len=10) "non-prod-d",
       (string) (len=1) "a": (string) (len=10) "non-prod-a"
      },
      Dvars: (impl.Dvars) (len=2 cap=2) {
       (impl.Dvar) {
        Name: (string) (len=9) "dvar_np_a",
        Value: (string) (len=6) "{{.a}}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       },
       (impl.Dvar) {
        Name: (string) (len=3) "dab",
        Value: (string) (len=17) "{{.a}}-and-{{.b}}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
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
     }
    })
    
    [global] dvar expanded result:
    {
      "da": "global-a",
      "dab": "global-a-and-global-b"
    }
    
    
    scope[global] merged: {
      "e": "global-e",
      "da": "global-a",
      "dab": "global-a-and-global-b",
      "a": "global-a",
      "b": "global-b",
      "c": "global-c"
    }
    
    
    [nonprod] dvar expanded result:
    {
      "dvar_np_a": "non-prod-a",
      "dab": "non-prod-a-and-non-prod-b"
    }
    
    
    scope[nonprod] merged: {
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "dvar_np_a": "non-prod-a"
    }
    
    
    ---------group vars----------
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "dvar_np_a": "non-prod-a",
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d"
    }
    
    
    global: {
      "b": "global-b",
      "c": "global-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "global-a-and-global-b",
      "a": "global-a"
    }
    
    
    groups members:[dev staging]
    module: [grave_pike6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "a": "non-prod-a",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e"
    }
    
    (core.Cache) (len=8) {
     (string) (len=1) "e": (string) (len=8) "global-e",
     (string) (len=2) "da": (string) (len=8) "global-a",
     (string) (len=3) "dab": (string) (len=25) "non-prod-a-and-non-prod-b",
     (string) (len=1) "a": (string) (len=10) "non-prod-a",
     (string) (len=1) "d": (string) (len=10) "non-prod-d",
     (string) (len=9) "dvar_np_a": (string) (len=10) "non-prod-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=1) "c": (string) (len=10) "non-prod-c"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "dab": "non-prod-a-and-non-prod-b",
      "a": "non-prod-a",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"cmd1:da -> {{.da}}\"",
        "echo \"cmd2:dab -> {{.dab}}\"",
        "echo \"cmd3:{{.dvar_np_a}}\""
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
      "dvar_np_a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "a": "non-prod-a",
      "d": "non-prod-d"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "a": "non-prod-a",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a"
    }
    
    
    grave_pike6: overall final exec vars:
    
    (*core.Cache)({
      "a": "non-prod-a",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b"
    })
    
    cmd( 1):
    echo "cmd1:da -> {{.da}}"
    
     \_ echo "cmd1:da -> global-a"
    cmd1:da -> global-a
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=19) "cmd1:da -> global-a",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "cmd2:dab -> {{.dab}}"
    
     \_ echo "cmd2:dab -> non-prod-a-and-non-prod-b"
    cmd2:dab -> non-prod-a-and-non-prod-b
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=37) "cmd2:dab -> non-prod-a-and-non-prod-b",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "cmd3:{{.dvar_np_a}}"
    
     \_ echo "cmd3:non-prod-a"
    cmd3:non-prod-a
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=15) "cmd3:non-prod-a",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0029 log - verbose level v](../../logs/c0029_v)
* [c0029 log - verbose level vv](../../logs/c0029_vv)
* [c0029 log - verbose level vvv](../../logs/c0029_vvv)
* [c0029 log - verbose level vvvv](../../logs/c0029_vvvv)
* [c0029 log - verbose level vvvvv](../../logs/c0029_vvvvv)

##### References
* [Related Chapter](../../dvars/c0029)
