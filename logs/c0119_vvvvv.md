---
title: "c0119_vvvvv"
date: 2020-07-20T02:01:50+77:00
draft: false
weight: 11194

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0119
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0119
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bd6e0)(<nil>)
    
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
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1: [step1: demo it will loop until loopitem = item3 ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "demo it will loop until loopitem = item3",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3",
        "item4"
      },
      Until: "{{ eq .loopitem \"item3\" }}",
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
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item1
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item2
    loop util conditional break
    
    -Step2: [step2:  ]
    {
      Name: "step2",
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
    })
    
    hello
    ~SubStep1: [print:  ]
    hello
    -Step3: [step3:  ]
    {
      Name: "step3",
      Do: "subtask",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "proc 1",
        "proc 2",
        "proc 3",
        "proc 4"
      },
      Until: "{{ eq .loopitem \"proc 3\" }}",
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
    
    caller's vars to task (subtask)::
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 1
    caller's vars to task (subtask)::
    (*core.Cache)({
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 2
    loop util conditional break
    
    -Step4: [step4:  ]
    {
      Name: "step4",
      Do: "subtask",
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "proc 1",
        "proc 2",
        "proc 3",
        "proc 4"
      },
      Until: "{{ eq .loopindex 3 }}",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (subtask)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 1",
      "loopindex": 0
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 1
    caller's vars to task (subtask)::
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 2"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 2
    caller's vars to task (subtask)::
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3"
    })
    
      located task-> 2 [subtask]: 
    =Task2: [task ==> subtask: subtask to test reg and return ]
    Executing task stack layer: 2
    
    --Step1: [step1: the loopitem here is inherited from caller ]
    {
      Name: "step1",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "the loopitem here is inherited from caller",
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    proc 3
    loop util conditional break
    
    -Step5: [step5: it will stop loop at proc 4 ]
    {
      Name: "step5",
      Do: "subtask2",
      Dox: <nil>,
      Func: "call",
      Vars: {
        "person": "jason"
      },
      Dvars: <nil>,
      Desc: "it will stop loop at proc 4",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "proc 1",
        "proc 2",
        "proc 3",
        "proc 4",
        "proc 5",
        "proc 6"
      },
      Until: "{{ eq .person \"tom\" }}",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "person": "jason",
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "jason",
      "up_runtime_task_layer_number": 1
    })
    
    caller's vars to task (subtask2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "name": "person",
            "value": "tom"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{ eq .loopindex 3 }}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        {
          "cmd": "person: {{.person}}",
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
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 1"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "person": "jason"
    })
    
    person: {{.person}}
    ~~SubStep1: [print:  ]
    person: jason
    caller's vars to task (subtask2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    })
    
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "name": "person",
            "value": "tom"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{ eq .loopindex 3 }}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        {
          "name": "print",
          "cmd": "person: {{.person}}"
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
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1,
      "loopindex1": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 2",
      "loopindex": 1
    })
    
    person: {{.person}}
    ~~SubStep1: [print:  ]
    person: jason
    caller's vars to task (subtask2)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "reg",
          "cmd": {
            "value": "tom",
            "name": "person"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{ eq .loopindex 3 }}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    condition failed, skip executing step 
    
    --Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        {
          "name": "print",
          "cmd": "person: {{.person}}"
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
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 3"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": "jason",
      "loopitem": "proc 3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1
    })
    
    person: {{.person}}
    ~~SubStep1: [print:  ]
    person: jason
    caller's vars to task (subtask2)::
    (*core.Cache)({
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 3 [subtask2]: 
    =Task3: [task ==> subtask2:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "name": "person",
            "value": "tom"
          },
          "name": "reg"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{ eq .loopindex 3 }}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "person": "jason",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    map[name:person value:tom]
    ~~SubStep1: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "tom",
      "loopitem": "proc 4",
      "loopindex": 3
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "tom",
      "loopitem": "proc 4"
    })
    
    --Step2: [step2:  ]
    {
      Name: "step2",
      Do: {
        {
          "name": "print",
          "cmd": "person: {{.person}}"
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
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": "tom",
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "proc 4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "person": "tom"
    })
    
    person: {{.person}}
    ~~SubStep1: [print:  ]
    person: tom
    loop util conditional break
    
    
```

##### Logs with different verbose level
* [c0119 log - verbose level v](../../logs/c0119_v)
* [c0119 log - verbose level vv](../../logs/c0119_vv)
* [c0119 log - verbose level vvv](../../logs/c0119_vvv)
* [c0119 log - verbose level vvvv](../../logs/c0119_vvvv)
* [c0119 log - verbose level vvvvv](../../logs/c0119_vvvvv)

##### References
* [Related Chapter](../../loop/c0119)
