---
title: "f0012_vvvvv"
date: 2020-07-01T15:35:00+77:00
draft: false
weight: 101204

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/modtests/f0012/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/modtests/f0012
                 WorkDir -> refdir
              AbsWorkDir -> /up_project/up/tests/modtests/f0012
                TaskFile -> up.yml
                 Verbose -> vvvvv
              ModuleName -> desperate_swartz9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 8
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/f0012
    -exec task: Main
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc00017afc0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [desperate_swartz9] instance id: [dev]
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
    
    
    desperate_swartz9: overall final exec vars:
    
    (*core.Cache)({
    })
    
    caller's vars to task (hello-module.Say_hello)::
    (*core.Cache)({
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000228380)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
          "name": "print",
          "cmd": "... hello"
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
    
    
    hello-module: overall final exec vars:
    
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
    
    
    hello-module: overall final exec vars:
    
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
    (*impl.Scopes)(0xc000229b60)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
     .... cross call 1
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    {
      Name: "",
      Do: "crosstalk2.Cross_call2",
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
      "up_runtime_tasker_layer_number": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 3
    }
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002bb380)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [crosstalk2] instance id: [nonamed]
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
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 4
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": " .... cross call 2"
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
      "up_runtime_tasker_layer_number": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 4
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
     .... cross call 2
    ~SubStep1: [print:  ]
     .... cross call 2
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
      "up_runtime_tasker_layer_number": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 4
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 4
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc00031eba0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    Executing tasker layer: 5
    
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
      "up_runtime_tasker_layer_number": 5
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 5
    }
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
     .... cross call 1
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    {
      Name: "",
      Do: "crosstalk2.Cross_call2",
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
      "up_runtime_tasker_layer_number": 5
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 5
    }
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 5
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0003903c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [crosstalk2] instance id: [nonamed]
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
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 6
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": " .... cross call 2"
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
      "up_runtime_tasker_layer_number": 6
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 6
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
     .... cross call 2
    ~SubStep1: [print:  ]
     .... cross call 2
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
      "up_runtime_tasker_layer_number": 6
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 6
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000391be0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    Executing tasker layer: 7
    
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
      "up_runtime_tasker_layer_number": 7
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 7
    }
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
     .... cross call 1
    ~SubStep1: [print:  ]
     .... cross call 1
    -Step2:
    {
      Name: "",
      Do: "crosstalk2.Cross_call2",
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
      "up_runtime_tasker_layer_number": 7
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 7
    }
    
    
    crosstalk1: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc0003d9400)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [crosstalk2] instance id: [nonamed]
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
    
    =>call module: [crosstalk2] task: [Cross_call2]
    Executing tasker layer: 8
    
      located task-> 3 [Cross_call2]: 
    Task3: [TODO: Main Caller Taskname ==> Cross_call2:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": " .... cross call 2",
          "name": "print"
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
      "up_runtime_tasker_layer_number": 8
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 8
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
     .... cross call 2
    ~SubStep1: [print:  ]
     .... cross call 2
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
      "up_runtime_tasker_layer_number": 8
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 8
    }
    
    
    crosstalk2: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    -------full vars in scopes------
    (*impl.Scopes)(0xc000454c20)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    Executing tasker layer: 9
    
          Module call layer check: -> Too many layers of recursive module executions, max allowed(8), please fix your recursive call
    -----trace for reference-----
    
```

##### Logs with different verbose level
* [mf0012 log - verbose level v](../../logs/mf0012_v)
* [mf0012 log - verbose level vv](../../logs/mf0012_vv)
* [mf0012 log - verbose level vvv](../../logs/mf0012_vvv)
* [mf0012 log - verbose level vvvv](../../logs/mf0012_vvvv)
* [mf0012 log - verbose level vvvvv](../../logs/mf0012_vvvvv)

##### References
* [Related Chapter](../../module/f0012)
