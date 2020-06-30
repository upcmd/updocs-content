---
title: "c0142_vvvv"
date: 2020-07-01T15:34:42+77:00
draft: false
weight: 11423

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0142
                 Verbose -> vvvv
              ModuleName -> hopeful_turing9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0142
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hopeful_turing9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "msg": "hello, world",
            "bg": "blue",
            "fg": "white"
          },
          "name": "colorprint"
        },
        {
          "name": "colorprint",
          "cmd": {
            "msg": "hello, world",
            "bg": "yellow"
          }
        },
        {
          "cmd": {
            "msg": "hello, world",
            "fg": "white"
          },
          "name": "colorprint"
        },
        {
          "name": "colorprint",
          "cmd": {
            "msg": "hello, world"
          }
        },
        {
          "name": "colorprint",
          "cmd": {
            "msg": "{{.person.name}}: {{.person.age}}",
            "fg": "blue",
            "bg": "red"
          }
        },
        {
          "name": "colorprint",
          "cmd": {
            "object": "person",
            "fg": "blue",
            "bg": "black"
          }
        },
        {
          "name": "colorprint",
          "cmd": {
            "fg": "blue",
            "bg": "green",
            "object": "{{.objectname}}"
          }
        },
        {
          "name": "colorprint",
          "cmd": {
            "msg": "person",
            "fg": "blue",
            "bg": "black",
            "object": "person"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": {
          "name": "tom",
          "age": 18
        },
        "objectname": "person"
      },
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
      "objectname": "person",
      "person": {
        "age": 18,
        "name": "tom"
      }
    })
    
    hopeful_turing9: overall final exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "age": 18
      },
      "objectname": "person"
    })
    
    ~SubStep1: [colorprint:  ]
    37 44
    hello, world
    ~SubStep2: [colorprint:  ]
    37 44
    hello, world
    ~SubStep3: [colorprint:  ]
    37 44
    hello, world
    ~SubStep4: [colorprint:  ]
    37 44
    hello, world
    ~SubStep5: [colorprint:  ]
    37 44
    tom: 18
    ~SubStep6: [colorprint:  ]
    37 44
    object person:
     {
      "age": 18,
      "name": "tom"
    }
    
    ~SubStep7: [colorprint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    ~SubStep8: [colorprint:  ]
    37 44
     WARN: [colorprint] - [msg and object can not coexist]
    
```

##### Logs with different verbose level
* [c0142 log - verbose level v](../../logs/c0142_v)
* [c0142 log - verbose level vv](../../logs/c0142_vv)
* [c0142 log - verbose level vvv](../../logs/c0142_vvv)
* [c0142 log - verbose level vvvv](../../logs/c0142_vvvv)
* [c0142 log - verbose level vvvvv](../../logs/c0142_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0142)
