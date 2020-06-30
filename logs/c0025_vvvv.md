---
title: "c0025_vvvv"
date: 2020-07-01T15:34:24+77:00
draft: false
weight: 10253

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0025
                 Verbose -> vvvv
              ModuleName -> dreamy_tesla5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0025
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [dreamy_tesla5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"a smart guy=>{{.a_smart_guy}}\"\"\""
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    })
    
    dreamy_tesla5: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
     \_ echo """a smart guy=>name: "Tom"
    sex: "Male"
    school: "Sydney Grammar"
    """
    a smart guy=>name: Tom
    sex: Male
    school: Sydney Grammar
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0025 log - verbose level v](../../logs/c0025_v)
* [c0025 log - verbose level vv](../../logs/c0025_vv)
* [c0025 log - verbose level vvv](../../logs/c0025_vvv)
* [c0025 log - verbose level vvvv](../../logs/c0025_vvvv)
* [c0025 log - verbose level vvvvv](../../logs/c0025_vvvvv)

##### References
* [Related Chapter](../../dvars/c0025)
