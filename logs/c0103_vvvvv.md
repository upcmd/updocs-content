---
title: "c0103_vvvvv"
date: 2020-06-25T01:55:57+66:00
draft: false
weight: 11034

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
                 Verbose -> vvvvv
              ModuleName -> mad_mclean5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0103
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f2f40)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [mad_mclean5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    }
    
    (core.Cache) (len=2) {
     (string) (len=3) "tom": (string) (len=27) "tom:\n  sex: male\n  age: 23\n",
     (string) (len=5) "emily": (string) (len=31) "emily:\n  sex: female\n  age: 32\n"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
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
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    }
    
    
    mad_mclean5: overall final exec vars:
    
    (*core.Cache)({
      "emily": "emily:\n  sex: female\n  age: 32\n",
      "tom": "tom:\n  sex: male\n  age: 23\n"
    })
    
    map[path:tom.sex reg:tomyml value:female verbose:v ymlstr:{{.tom}}]
    ~SubStep1: [yml_write:  ]
    yml modified:
    
    "tom:\n  sex: female\n  age: 23\n"
    
    {{.tomyml }}
    ~SubStep2: [print:  ]
    tom:
      sex: female
      age: 23
    
    map[nodevalue:{{.emily}} path:tom.wife reg:tomyml verbose:vvvv ymlstr:{{.tomyml}}]
    ~SubStep3: [yml_write:  ]
    yml modified:
    
    "tom:\n  sex: female\n  age: 23\n  wife:\n    emily:\n      sex: female\n      age: 32\n"
    
    {{.tomyml }}
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
