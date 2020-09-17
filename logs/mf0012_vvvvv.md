---
title: "f0012_vvvvv"
date: 2020-09-18T01:28:28+99:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 8
               EntryTask -> Main
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up/tests/modtests/f0012
    -exec task: Main
    loading [Task]:  ./up.yml
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000204220)(<nil>)
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (hello-module.Say_hello)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [hello-module], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000205440)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_task_layer_number": 0,
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 2,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    }
    
    
    hello-module: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 2
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002ecec0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 3,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 3,
      "up_runtime_task_layer_number": 0
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 3,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 3
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 3
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0003fc880)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 4,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 4
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 4
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 4
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002046c0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 5
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002ec9e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 6
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6,
      "up_runtime_task_layer_number": 0
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 6
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 6
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 6
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 6,
      "up_runtime_task_layer_number": 0
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002ed1a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
          "cmd": " .... cross call 1",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 7,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 7,
      "up_runtime_task_layer_number": 0
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 7
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 7
    }
    
    
    crosstalk1: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 7
    })
    
    caller's vars to task (crosstalk2.Cross_call2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 7
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk2], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000c280)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_tasker_layer_number": 8,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 8,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 8
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_tasker_layer_number": 8,
      "up_runtime_task_layer_number": 0
    }
    
    
    crosstalk2: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 8
    })
    
    caller's vars to task (crosstalk1.Cross_call1)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_tasker_layer_number": 8
    })
    
    loading [Config]:  ./upconfig.yml
    loading [Task]:  ./up.yml
    module: [crosstalk1], instance id: [nonamed], exec profile: []
     WARN: [*be aware*] - [both instance id and exec profile are not set]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002ed060)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
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
    
    Recovered from: runtime error: invalid memory address or nil pointer dereference
     WARN: [Not rescued in task level] - [please assess the panic problem and cause, fix it before re-run the task]
    task finally -> runtime error: invalid memory address or nil pointer dereference
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
