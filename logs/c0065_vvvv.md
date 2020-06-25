---
title: "c0065_vvvv"
date: 2020-06-25T01:55:47+66:00
draft: false
weight: 10653

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0065
                 Verbose -> vvvv
              ModuleName -> happy_leakey0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0065
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [happy_leakey0] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    dvar> var_with_range_v:
    " x  x  x "
    
    dvar> var_with_range_vv:
    " x  x  x "
    
    dvar> var_with_range_vvv:
    " x  x  x "
    
    dvar> var_with_range_vvvv:
    " x  x  x "
    
    dvar> var_with_range_vvvvv:
    " x  x  x "
    
    dvar> var_with_range_vvvvv:
    " x  x  x "
    
    -------runtime global final merged with dvars-------
    
    {
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_range_vvvv": " x  x  x ",
      "var_with_range_vvvvv": " x  x  x ",
      "var_with_range_vvvvvv": " x  x  x ",
      "var_with_range_v": " x  x  x ",
      "var_with_range_vv": " x  x  x ",
      "var_with_range_vvv": " x  x  x ",
      "person": "peter"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [c0065 log - verbose level v](../../logs/c0065_v)
* [c0065 log - verbose level vv](../../logs/c0065_vv)
* [c0065 log - verbose level vvv](../../logs/c0065_vvv)
* [c0065 log - verbose level vvvv](../../logs/c0065_vvvv)
* [c0065 log - verbose level vvvvv](../../logs/c0065_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0065)
