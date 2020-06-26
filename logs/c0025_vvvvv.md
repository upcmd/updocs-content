---
title: "c0025_vvvvv"
date: 2020-06-27T03:09:16+66:00
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
              ModuleName -> angry_jones5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0025
    -------full vars in scopes------
    (*impl.Scopes)(0xc000182fc0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [angry_jones5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
      (string) (len=4) "name": (string) (len=3) "Tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    
    angry_jones5: overall final exec vars:
    
    (*core.Cache)({
      "a_smart_guy": "name: \"Tom\"\nsex: \"Male\"\nschool: \"Sydney Grammar\"\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
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
    (utils.ExecResult) {
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
