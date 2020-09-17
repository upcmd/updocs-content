---
title: "c0142_vvvvv"
date: 2020-09-18T01:27:47+99:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0142
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bd0e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
          "name": "colorPrint",
          "cmd": {
            "msg": "hello, world",
            "bg": "blue",
            "fg": "white"
          }
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
            "fg": "white",
            "msg": "hello, world"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      "person": {
        "name": "tom",
        "age": 18
      },
      "objectname": "person",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "objectname": "person",
      "up_runtime_task_layer_number": 0,
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
      "name": "tom",
      "age": 18
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
