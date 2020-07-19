---
title: "c0142_vvvvv"
date: 2020-07-20T02:01:55+77:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0142
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c7080)(<nil>)
    
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
            "fg": "white",
            "msg": "hello, world",
            "bg": "blue"
          },
          "name": "colorPrint"
        },
        {
          "name": "colorPrint",
          "cmd": {
            "msg": "hello, world",
            "bg": "yellow"
          }
        },
        {
          "name": "colorPrint",
          "cmd": {
            "msg": "hello, world",
            "fg": "white"
          }
        },
        {
          "name": "colorPrint",
          "cmd": {
            "msg": "hello, world"
          }
        },
        {
          "name": "colorPrint",
          "cmd": {
            "msg": "{{.person.name}}: {{.person.age}}",
            "fg": "blue",
            "bg": "red"
          }
        },
        {
          "name": "colorPrint",
          "cmd": {
            "fg": "blue",
            "bg": "black",
            "object": "person"
          }
        },
        {
          "name": "colorPrint",
          "cmd": {
            "object": "{{.objectname}}",
            "fg": "blue",
            "bg": "green"
          }
        },
        {
          "name": "colorPrint",
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
        "name": "tom",
        "age": 18
      }
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
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "objectname": "person",
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    map[bg:blue fg:white msg:hello, world]
    ~SubStep1: [colorPrint:  ]
    37 44
    hello, world
    map[bg:yellow msg:hello, world]
    ~SubStep2: [colorPrint:  ]
    37 44
    hello, world
    map[fg:white msg:hello, world]
    ~SubStep3: [colorPrint:  ]
    37 44
    hello, world
    map[msg:hello, world]
    ~SubStep4: [colorPrint:  ]
    37 44
    hello, world
    map[bg:red fg:blue msg:{{.person.name}}: {{.person.age}}]
    ~SubStep5: [colorPrint:  ]
    37 44
    tom: 18
    map[bg:black fg:blue object:person]
    ~SubStep6: [colorPrint:  ]
    37 44
    object person:
     {
      "age": 18,
      "name": "tom"
    }
    
    map[bg:green fg:blue object:{{.objectname}}]
    ~SubStep7: [colorPrint:  ]
    37 44
    object person:
     {
      "name": "tom",
      "age": 18
    }
    
    map[bg:black fg:blue msg:person object:person]
    ~SubStep8: [colorPrint:  ]
    37 44
     WARN: [colorPrint] - [msg and object can not coexist]
    
```

##### Logs with different verbose level
* [c0142 log - verbose level v](../../logs/c0142_v)
* [c0142 log - verbose level vv](../../logs/c0142_vv)
* [c0142 log - verbose level vvv](../../logs/c0142_vvv)
* [c0142 log - verbose level vvvv](../../logs/c0142_vvvv)
* [c0142 log - verbose level vvvvv](../../logs/c0142_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0142)
