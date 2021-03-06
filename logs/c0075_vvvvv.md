---
title: "c0075_vvvvv"
date: 2020-10-07T00:11:12+1010:00
draft: false
weight: 10754

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0075
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
    loading [Task]:  ./tests/functests/c0075
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf300)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    })
    
    (*core.Cache)(0xc00000e950)((len=2) {
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=6) "person": (string) (len=5) "peter"
    })
    
    dvar> var_with_range:
    " x  x  x "
    
    -
     x  x  x 
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
          template rendering -> template: .:1:26: executing "." at <.person>: can't evaluate field person in type interface {}
    WARN:
        1:{{range $x:=.managers}} {{.person}} {{end}}
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
    dvar> var_to_ref_to_outside_of_range_from_within_range:
    " "
    
    -
     
    dvar> var_directly_ref_to:
    "peter"
    
    -
    peter
    dvar> var_to_ref_to_outside_of_range_from_within_range_fixed:
    " peter  peter  peter "
    
    -
     peter  peter  peter 
    [runtime global] dvar expanded result:
    {
      "var_with_range": " x  x  x ",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_to_ref_to_outside_of_range_from_within_range": " ",
      "var_directly_ref_to": "peter",
      "var_to_ref_to_outside_of_range_from_within_range_fixed": " peter  peter  peter "
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "var_with_range": " x  x  x ",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_to_ref_to_outside_of_range_from_within_range": " ",
      "var_directly_ref_to": "peter",
      "var_to_ref_to_outside_of_range_from_within_range_fixed": " peter  peter  peter ",
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [c0075 log - verbose level v](../../logs/c0075_v)
* [c0075 log - verbose level vv](../../logs/c0075_vv)
* [c0075 log - verbose level vvv](../../logs/c0075_vvv)
* [c0075 log - verbose level vvvv](../../logs/c0075_vvvv)
* [c0075 log - verbose level vvvvv](../../logs/c0075_vvvvv)

##### References
* [Related Chapter](../../template/c0075)
