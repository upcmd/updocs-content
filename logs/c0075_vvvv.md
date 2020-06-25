---
title: "c0075_vvvv"
date: 2020-06-25T01:55:49+66:00
draft: false
weight: 10753

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
                 Verbose -> vvvv
              ModuleName -> angry_hodgkin6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0075
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [angry_hodgkin6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    dvar> var_with_range:
    " x  x  x "
    
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
          template rendering problem -> template: .:1:26: executing "." at <.person>: can't evaluate field person in type interface {}
    WARN:
        1:{{range $x:=.managers}} {{.person}} {{end}}
    
    -----trace for reference-----
    dvar> var_to_ref_to_outside_of_range_from_within_range:
    " "
    
    dvar> var_directly_ref_to:
    "peter"
    
    dvar> var_to_ref_to_outside_of_range_from_within_range_fixed:
    " peter  peter  peter "
    
    -------runtime global final merged with dvars-------
    
    {
      "var_to_ref_to_outside_of_range_from_within_range_fixed": " peter  peter  peter ",
      "var_with_range": " x  x  x ",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "person": "peter",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_to_ref_to_outside_of_range_from_within_range": " ",
      "var_directly_ref_to": "peter"
    }
    
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