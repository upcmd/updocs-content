---
title: "c0101_vvvv"
date: 2020-06-25T01:55:55+66:00
draft: false
weight: 11013

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0101
                 Verbose -> vvvv
              ModuleName -> naughty_stallman1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0101
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [naughty_stallman1] instance id: [dev]
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
          "name": "print",
          "cmd": "hello"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
    })
    
    naughty_stallman1: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    hello
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "pause"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
    })
    
    naughty_stallman1: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [pause:  ]
    Enter Value For pause action to continue: 
    
    enter: continue 
        q: quit
        i: inspect
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "world"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
    })
    
    naughty_stallman1: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    world
    
```

##### Logs with different verbose level
* [c0101 log - verbose level v](../../logs/c0101_v)
* [c0101 log - verbose level vv](../../logs/c0101_vv)
* [c0101 log - verbose level vvv](../../logs/c0101_vvv)
* [c0101 log - verbose level vvvv](../../logs/c0101_vvvv)
* [c0101 log - verbose level vvvvv](../../logs/c0101_vvvvv)

##### References
* [Related Chapter](../../test-debug/c0101)