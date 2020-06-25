---
title: "c0010_vvvv"
date: 2020-06-25T01:55:38+66:00
draft: false
weight: 10103

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
                 Verbose -> vvvv
              ModuleName -> berserk_ritchie2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0010
    ---------group vars----------
    
    prod: {
      "c": "prod-c",
      "a": "prod-a"
    }
    
    
    nonprod: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": {
        "c3": {
          "c32": "nonprod-c32",
          "c33": "nonprod-c33"
        },
        "c4": "nonprod-c4",
        "c5": "nonprod-c5",
        "c1": "nonprod-c1",
        "c2": "nonprod-c2"
      }
    }
    
    
    global: {
      "c": {
        "c3": {
          "c31": "global-c31",
          "c32": "global-c32",
          "c33": "global-c33"
        },
        "c4": "global-c4",
        "c1": "global-c1",
        "c2": "global-c2"
      },
      "d": "global-d",
      "a": "global-a",
      "b": "global-b"
    }
    
    
    groups members:[dr prod dev st staging]
    module: [berserk_ritchie2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c32": "nonprod-c32",
          "c33": "dev-c33",
          "c31": "global-c31"
        },
        "c4": "nonprod-c4"
      },
      "d": "global-d"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": {
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2",
        "c3": {
          "c31": "global-c31",
          "c32": "nonprod-c32",
          "c33": "dev-c33"
        },
        "c4": "nonprod-c4"
      },
      "d": "global-d"
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
      "c": {
        "c3": {
          "c31": "global-c31",
          "c32": "nonprod-c32",
          "c33": "dev-c33"
        },
        "c4": "nonprod-c4",
        "c1": "dev-c1",
        "c5": "nonprod-c5",
        "c6": "dev-c6",
        "c7": "dev-c7",
        "c2": "dev-c2"
      },
      "d": "global-d"
    })
    
    berserk_ritchie2: overall final exec vars:
    
    (*core.Cache)({
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
    
     \_ echo "test out the var scopes only"
    test out the var scopes only
     .. ok
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
