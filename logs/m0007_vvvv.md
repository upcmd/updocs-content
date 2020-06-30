---
title: "0007_vvvv"
date: 2020-07-01T15:34:58+77:00
draft: false
weight: 100703

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0007/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0007
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0007
                TaskFile -> up.yml
                 Verbose -> vvvv
              ModuleName -> sad_shockley7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up/tests/modtests/0007
    -exec task: Main
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sad_shockley7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1: [: note that the module dir is: hello-module, but in upconfig.yml you give the alias hello as module name
     ]
    {
      Name: "",
      Do: "hello.Say_world",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "note that the module dir is: hello-module, but in upconfig.yml you give the alias hello as module name\n",
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
    
    sad_shockley7: overall final exec vars:
    
    (*core.Cache)({
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hello] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
    =>call module: [hello] task: [Say_world]
    Executing tasker layer: 2
    
      located task-> 2 [Say_world]: 
    Task2: [TODO: Main Caller Taskname ==> Say_world:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": " .... world from Say_world"
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
      "up_runtime_tasker_layer_number": 2
    })
    
    hello: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
    ~SubStep1: [print:  ]
     .... world from Say_world
    
```

##### Logs with different verbose level
* [m0007 log - verbose level v](../../logs/m0007_v)
* [m0007 log - verbose level vv](../../logs/m0007_vv)
* [m0007 log - verbose level vvv](../../logs/m0007_vvv)
* [m0007 log - verbose level vvvv](../../logs/m0007_vvvv)
* [m0007 log - verbose level vvvvv](../../logs/m0007_vvvvv)

##### References
* [Related Chapter](../../module/0007)
