---
title: "c0029_vvvv"
date: 2020-07-01T15:34:24+77:00
draft: false
weight: 10293

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
                 Verbose -> vvvv
              ModuleName -> high_hypatia2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0029
    ---------group vars----------
    
    global: {
      "a": "global-a",
      "b": "global-b",
      "c": "global-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "global-a-and-global-b"
    }
    
    
    nonprod: {
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "dab": "non-prod-a-and-non-prod-b",
      "dvar_np_a": "non-prod-a"
    }
    
    
    groups members:[dev staging]
    module: [high_hypatia2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "dvar_np_a": "non-prod-a",
      "d": "non-prod-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "dvar_np_a": "non-prod-a",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
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
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "dvar_np_a": "non-prod-a",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e"
    })
    
    high_hypatia2: overall final exec vars:
    
    (*core.Cache)({
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "dvar_np_a": "non-prod-a",
      "d": "non-prod-d"
    })
    
    cmd( 1):
    echo "cmd1:da -> {{.da}}"
    
     \_ echo "cmd1:da -> global-a"
    cmd1:da -> global-a
     .. ok
    cmd( 2):
    echo "cmd2:dab -> {{.dab}}"
    
     \_ echo "cmd2:dab -> non-prod-a-and-non-prod-b"
    cmd2:dab -> non-prod-a-and-non-prod-b
     .. ok
    cmd( 3):
    echo "cmd3:{{.dvar_np_a}}"
    
     \_ echo "cmd3:non-prod-a"
    cmd3:non-prod-a
     .. ok
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
