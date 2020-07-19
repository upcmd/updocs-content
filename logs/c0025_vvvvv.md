---
title: "c0025_vvvvv"
date: 2020-07-20T02:01:33+77:00
draft: false
weight: 10254

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0025
    -------full vars in scopes------
    (*impl.Scopes)(0xc000174fe0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
     }
    }
    
    [runtime global] dvar expanded result:
    {
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
    cmd=>:
    echo """a smart guy=>name: "Tom"
    sex: "Male"
    school: "Sydney Grammar"
    """<=
    a smart guy=>name: Tom
    sex: Male
    school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=73) "echo \"\"\"a smart guy=>name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=55) "a smart guy=>name: Tom\nsex: Male\nschool: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
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
