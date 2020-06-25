---
title: "c0103_vvvv"
date: 2020-06-25T01:55:57+66:00
draft: false
weight: 11033

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0103
                 Verbose -> vvvv
              ModuleName -> ecstatic_noyce5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0103
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [ecstatic_noyce5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: inplace modification ]
    {
      Name: "",
      Do: {
        {
          "name": "yml_write",
          "cmd": {
            "ymlstr": "{{.tom}}",
            "path": "tom.sex",
            "value": "female",
            "verbose": "v",
            "reg": "tomyml"
          }
        },
        {
          "name": "print",
          "cmd": "{{.tomyml }}"
        },
        {
          "name": "yml_write",
          "cmd": {
            "ymlstr": "{{.tomyml}}",
            "path": "tom.wife",
            "nodevalue": "{{.emily}}",
            "verbose": "vvvv",
            "reg": "tomyml"
          }
        },
        {
          "name": "print",
          "cmd": "{{.tomyml }}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inplace modification",
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
      "tom": "tom:\n  sex: male\n  age: 23\n",
      "emily": "emily:\n  sex: female\n  age: 32\n"
    })
    
    ecstatic_noyce5: overall final exec vars:
    
    (*core.Cache)({
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    })
    
    ~SubStep1: [yml_write:  ]
    ~SubStep2: [print:  ]
    tom:
      sex: female
      age: 23
    
    ~SubStep3: [yml_write:  ]
    ~SubStep4: [print:  ]
    tom:
      sex: female
      age: 23
      wife:
        emily:
          sex: female
          age: 32
    
    
```

##### Logs with different verbose level
* [c0103 log - verbose level v](../../logs/c0103_v)
* [c0103 log - verbose level vv](../../logs/c0103_vv)
* [c0103 log - verbose level vvv](../../logs/c0103_vvv)
* [c0103 log - verbose level vvvv](../../logs/c0103_vvvv)
* [c0103 log - verbose level vvvvv](../../logs/c0103_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0103)
