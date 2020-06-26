---
title: "c0065_vvvvv"
date: 2020-06-27T03:09:22+66:00
draft: false
weight: 10654

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
                 Verbose -> vvvvv
              ModuleName -> determined_darwin8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0065
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001cf220)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_darwin8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    (core.Cache) (len=2) {
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=6) "person": (string) (len=5) "peter"
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
    
    [runtime global] dvar expanded result:
    {
      "var_with_range_vvvv": " x  x  x ",
      "var_with_range_vvvvv": " x  x  x ",
      "var_with_range_vvvvvv": " x  x  x ",
      "var_with_range_v": " x  x  x ",
      "var_with_range_vv": " x  x  x ",
      "var_with_range_vvv": " x  x  x "
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "var_with_range_vvv": " x  x  x ",
      "var_with_range_vvvv": " x  x  x ",
      "var_with_range_vvvvv": " x  x  x ",
      "var_with_range_vvvvvv": " x  x  x ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "person": "peter",
      "var_with_range_v": " x  x  x ",
      "var_with_range_vv": " x  x  x "
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
