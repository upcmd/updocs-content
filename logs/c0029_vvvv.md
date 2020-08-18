---
title: "c0029_vvvv"
date: 2020-08-18T15:15:52+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0029
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: {
      "dvar_np_a": "non-prod-a",
      "dab": "non-prod-a-and-non-prod-b",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d"
    }
    
    
    global: {
      "a": "global-a",
      "b": "global-b",
      "c": "global-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "global-a-and-global-b"
    }
    
    
    groups members:[dev staging]
    merged[ dev ] runtime vars:
    {
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a",
      "a": "non-prod-a",
      "b": "non-prod-b"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "e": "global-e",
      "da": "global-a",
      "dab": "non-prod-a-and-non-prod-b",
      "d": "non-prod-d",
      "dvar_np_a": "non-prod-a"
    })
    
    cmd( 1):
    echo "cmd1:da -> {{.da}}"
    
    cmd=>:
    echo "cmd1:da -> global-a"
    -
    cmd1:da -> global-a
    -
     .. ok
    cmd( 2):
    echo "cmd2:dab -> {{.dab}}"
    
    cmd=>:
    echo "cmd2:dab -> non-prod-a-and-non-prod-b"
    -
    cmd2:dab -> non-prod-a-and-non-prod-b
    -
     .. ok
    cmd( 3):
    echo "cmd3:{{.dvar_np_a}}"
    
    cmd=>:
    echo "cmd3:non-prod-a"
    -
    cmd3:non-prod-a
    -
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
