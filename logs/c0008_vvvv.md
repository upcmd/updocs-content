---
title: "c0008_vvvv"
date: 2020-06-25T01:55:37+66:00
draft: false
weight: 10083

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
                 Verbose -> vvvv
              ModuleName -> mad_meitner3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0008
    ---------group vars----------
    
    nonprod: {
      "c": "non-prod-c",
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
    
    global: {
      "a": "global-a",
      "b": "global-b",
      "c": "global-c",
      "d": "global-d"
    }
    
    
    prod: {
      "a": "prod-a",
      "c": "prod-c"
    }
    
    
    groups members:[dr prod dev st staging]
    module: [mad_meitner3] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d"
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
      "b": "non-prod-b",
      "c": "dev-c",
      "d": "global-d",
      "a": "dev-a"
    })
    
    mad_meitner3: overall final exec vars:
    
    (*core.Cache)({
      "d": "global-d",
      "a": "dev-a",
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
* [c0008 log - verbose level v](../../logs/c0008_v)
* [c0008 log - verbose level vv](../../logs/c0008_vv)
* [c0008 log - verbose level vvv](../../logs/c0008_vvv)
* [c0008 log - verbose level vvvv](../../logs/c0008_vvvv)
* [c0008 log - verbose level vvvvv](../../logs/c0008_vvvvv)

##### References
* [Related Chapter](../../scope/c0008)