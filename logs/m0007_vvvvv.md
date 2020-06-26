---
title: "0007_vvvvv"
date: 2020-06-27T03:09:47+66:00
draft: false
weight: 100704

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
                 Verbose -> vvvvv
              ModuleName -> sleepy_mcclintock4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0007
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000240760)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sleepy_mcclintock4] instance id: [dev]
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    sleepy_mcclintock4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (hello.Say_world)::
    (*core.Cache)({
    })
    
     WARN: [config file does not exist] - [use builtin defaults]
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000241300)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [hello] instance id: [nonamed]
    merged[ nonamed ] runtime vars:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
     .... world from Say_world
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
