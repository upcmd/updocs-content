---
title: "0013_vvvvv"
date: 2020-07-20T02:02:16+77:00
draft: false
weight: 101304

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/0013/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/0013
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/0013
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 8
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/0013
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000174d40)(<nil>)
    
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
    
      located task-> 1 [Main]: 
    Task1: [Main ==> Main: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "hello-module.Say_hello",
      Dox: <nil>,
      Func: "call",
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (hello-module.Say_hello)::
    (*core.Cache)({
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175d40)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [hello-module] instance id: [nonamed]
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
    
    =>call module: [hello-module] task: [Say_hello]
    Executing tasker layer: 2
    
      located task-> 2 [Say_hello]: 
    Task2: [TODO: Main Caller Taskname ==> Say_hello:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "... hello",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "a": "aaa"
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
      "a": "aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_tasker_layer_number": 2
    })
    
    ... hello
    ~SubStep1: [print:  ]
    ... hello
    -Step2:
    {
      Name: "",
      Do: "crosstalk1.Cross_call1",
      Dox: <nil>,
      Func: "call",
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
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef600)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [crosstalk1] instance id: [nonamed]
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
    
    =>call module: [crosstalk1] task: [Cross_call1]
    Executing tasker layer: 3
    
      located task-> 3 [Cross_call1]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call1:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": " .... cross call 1"
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
      "up_runtime_tasker_layer_number": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 3
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
     .... cross call 1
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2: [: deactivated ]
    {
      Name: "",
      Do: <nil>,
      Dox: "crosstalk2.Cross_call2",
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "deactivated",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
     WARN: [*] - [Step is deactivated!]
    
```

##### Logs with different verbose level
* [m0013 log - verbose level v](../../logs/m0013_v)
* [m0013 log - verbose level vv](../../logs/m0013_vv)
* [m0013 log - verbose level vvv](../../logs/m0013_vvv)
* [m0013 log - verbose level vvvv](../../logs/m0013_vvvv)
* [m0013 log - verbose level vvvvv](../../logs/m0013_vvvvv)

##### References
* [Related Chapter](../../module/0013)
