---
title: "c0011_vvvv"
date: 2020-06-27T03:09:15+66:00
draft: false
weight: 10113

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
                 Verbose -> vvvv
              ModuleName -> pensive_wozniak7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0011
    ---------group vars----------
    
    prod: {
      "a": "prod-a",
      "c": "prod-c"
    }
    
    
    nonprod: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "a": "non-prod-a"
    }
    
    
    global: {
      "b": "global-b",
      "c": "global-c",
      "d": "global-d",
      "a": "global-a"
    }
    
    
    groups members:[dr prod dev st staging]
    module: [pensive_wozniak7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "runtime-a",
      "e": "runtime-e",
      "k": "runtime-k",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
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
      "c": "dev-c",
      "d": "global-d",
      "a": "runtime-a",
      "e": "local-e",
      "k": "runtime-k",
      "m": "local-m"
    })
    
    pensive_wozniak7: overall final exec vars:
    
    (*core.Cache)({
      "d": "global-d",
      "a": "runtime-a",
      "e": "local-e",
      "k": "runtime-k",
      "m": "local-m",
      "b": "non-prod-b",
      "c": "dev-c"
    })
    
    cmd( 1):
    echo "test out the var scopes only"
    
     \_ echo "test out the var scopes only"
    test out the var scopes only
     .. ok
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
