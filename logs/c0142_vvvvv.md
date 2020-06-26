---
title: "c0142_vvvvv"
date: 2020-06-27T03:09:34+66:00
draft: false
weight: 11424

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
                 Verbose -> vvvvv
              ModuleName -> adoring_bohr9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0142
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed000)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [adoring_bohr9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
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
            "bg": "blue",
            "fg": "white",
            "msg": "hello, world"
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
          "name": "colorprint",
          "cmd": {
            "msg": "hello, world",
            "fg": "white"
          }
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
            "object": "person",
            "msg": "person",
            "fg": "blue",
            "bg": "black"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": {
          "age": 18,
          "name": "tom"
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
      "person": {
        "name": "tom",
        "age": 18
      },
      "objectname": "person"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "objectname": "person",
      "person": {
        "name": "tom",
        "age": 18
      }
    }
    
    
    adoring_bohr9: overall final exec vars:
    
    (*core.Cache)({
      "objectname": "person",
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    map[bg:blue fg:white msg:hello, world]
    ~SubStep1: [colorprint:  ]
    37 44
    hello, world
    map[bg:yellow msg:hello, world]
    ~SubStep2: [colorprint:  ]
    37 44
    hello, world
    map[fg:white msg:hello, world]
    ~SubStep3: [colorprint:  ]
    37 44
    hello, world
    map[msg:hello, world]
    ~SubStep4: [colorprint:  ]
    37 44
    hello, world
    map[bg:red fg:blue msg:{{.person.name}}: {{.person.age}}]
    ~SubStep5: [colorprint:  ]
    37 44
    tom: 18
    map[bg:black fg:blue object:person]
    ~SubStep6: [colorprint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    map[bg:green fg:blue object:{{.objectname}}]
    ~SubStep7: [colorprint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    map[bg:black fg:blue msg:person object:person]
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
