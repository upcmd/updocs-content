---
title: "c0181_vvvvv"
date: 2020-10-06T23:46:26+1010:00
draft: false
weight: 11814

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0181
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0181
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bfc80)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e978)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    break loop using until condition
    ]
    {
      Name: "",
      Do: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "{{.loopitem}}"
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "break loop using until condition\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3",
        "item4",
        "item5",
        "item6"
      },
      Until: "{{eq .loopitem \"item4\"}}",
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
    
    -Step1:
    {
      Name: "",
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
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0,
      "loopitem": "item1"
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item1
    -Step1:
    {
      Name: "",
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
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "item2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "loopitem": "item2",
      "up_runtime_task_layer_number": 0,
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 1,
      "loopindex1": 2,
      "loopitem": "item2",
      "up_runtime_task_layer_number": 0
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item2
    -Step1:
    {
      Name: "",
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
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item3
    loop util conditional break
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "----------------------------------------------------"
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
    
    ----------------------------------------------------
    ~SubStep1: [print:  ]
    ----------------------------------------------------
    -Step3: [
    in this case the until condition will use a var which is chaning in block func
    in order to make the interal var accessible by parent block func, you will have to use return cmd to return the value, otherwise the block func can not use right changing value in the condition
    also the_internal_var has be be defined somewhere: scope/global/local, otherwise it will result in a golang templating error
    ]
    {
      Name: "",
      Do: {
        {
          "do": {
            {
              "name": "print",
              "cmd": "{{.loopitem}}"
            },
            {
              "name": "return",
              "cmd": {
                "the_internal_var"
              }
            }
          },
          "func": "cmd",
          "dvars": {
            {
              "flags": {
                "taskScope"
              },
              "name": "the_internal_var",
              "value": "{{.loopitem}}"
            }
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "post process {{.the_internal_var}} to see if this is executed"
            }
          }
        }
      },
      Dox: <nil>,
      Func: "block",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var",
          Value: "None",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "in this case the until condition will use a var which is chaning in block func\nin order to make the interal var accessible by parent block func, you will have to use return cmd to return the value, otherwise the block func can not use right changing value in the condition\nalso the_internal_var has be be defined somewhere: scope/global/local, otherwise it will result in a golang templating error\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3",
        "item4",
        "item5",
        "item6"
      },
      Until: "{{eq .the_internal_var \"item4\"}}",
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
      "the_internal_var": "None"
    }
    
    
    scope[local] merged: {
      "the_internal_var": "None",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "None",
      "up_runtime_task_layer_number": 0
    })
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var": "item1"
    }
    
    
    scope[local] merged: {
      "the_internal_var": "item1",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item1
    [the_internal_var]
    ~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var": "item1"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "post process {{.the_internal_var}} to see if this is executed"
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
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    post process {{.the_internal_var}} to see if this is executed
    ~SubStep1: [print:  ]
    post process None to see if this is executed
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var": "item1",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var": "item2"
    }
    
    
    scope[local] merged: {
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2",
      "loopitem": "item2"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2"
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item2
    [the_internal_var]
    ~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var": "item2"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "post process {{.the_internal_var}} to see if this is executed"
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
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item1"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "the_internal_var": "item1",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item1",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0
    })
    
    post process {{.the_internal_var}} to see if this is executed
    ~SubStep1: [print:  ]
    post process item1 to see if this is executed
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "cmd": {
            "the_internal_var"
          },
          "name": "return"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var": "item2",
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "item3"
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var": "item3"
    }
    
    
    scope[local] merged: {
      "loopindex1": 3,
      "loopitem": "item3",
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopindex": 2
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "loopitem": "item3",
      "up_runtime_task_layer_number": 0
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item3
    [the_internal_var]
    ~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var": "item3"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "post process {{.the_internal_var}} to see if this is executed"
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
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item2"
    })
    
    post process {{.the_internal_var}} to see if this is executed
    ~SubStep1: [print:  ]
    post process item2 to see if this is executed
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var": "item4"
    }
    
    
    scope[local] merged: {
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "loopitem": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    })
    
    {{.loopitem}}
    ~SubStep1: [print:  ]
    item4
    [the_internal_var]
    ~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var": "item4"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "post process {{.the_internal_var}} to see if this is executed"
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
      "loopindex1": 4,
      "loopitem": "item4",
      "loopindex": 3,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "loopitem": "item4",
      "loopindex": 3,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item3",
      "loopindex1": 4
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item3",
      "loopindex1": 4,
      "loopitem": "item4",
      "loopindex": 3,
      "up_runtime_task_layer_number": 0
    })
    
    post process {{.the_internal_var}} to see if this is executed
    ~SubStep1: [print:  ]
    post process item3 to see if this is executed
    loop util conditional break
    
    -Step4:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "----------------------------------------------------"
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
      "the_internal_var": "item4"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    })
    
    ----------------------------------------------------
    ~SubStep1: [print:  ]
    ----------------------------------------------------
    -Step5:
    {
      Name: "",
      Do: "sub_task",
      Dox: <nil>,
      Func: "call",
      Vars: {
        "the_internal_var2": "None"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: {
        "item1",
        "item2",
        "item3",
        "item4",
        "item5",
        "item6"
      },
      Until: "{{eq .the_internal_var2 \"item4\"}}",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "None"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "the_internal_var2": "None",
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item4",
      "the_internal_var2": "None",
      "up_runtime_task_layer_number": 0
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "None"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var2"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var2",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var": "item4",
      "the_internal_var2": "None",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var2": "item1"
    }
    
    
    scope[local] merged: {
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item1",
      "loopitem": "item1",
      "loopindex": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var": "item4",
      "the_internal_var2": "item1",
      "loopitem": "item1",
      "loopindex": 0,
      "loopindex1": 1,
      "up_runtime_task_layer_number": 1
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item1
    [the_internal_var2]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var2": "item1"
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "loopindex1": 2,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "item1",
      "loopitem": "item2",
      "loopindex": 1
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var2"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var2",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "the_internal_var2": "item1",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var2": "item2"
    }
    
    
    scope[local] merged: {
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item2",
      "loopitem": "item2",
      "loopindex": 1
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var2": "item2",
      "loopitem": "item2",
      "loopindex": 1,
      "loopindex1": 2,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item2
    [the_internal_var2]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var2": "item2"
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4",
      "the_internal_var2": "item2",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.loopitem}}"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var2"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var2",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item2",
      "loopitem": "item3",
      "loopindex": 2
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var2": "item3"
    }
    
    
    scope[local] merged: {
      "the_internal_var2": "item3",
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "item3",
      "loopindex": 2,
      "loopindex1": 3,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item3"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item3
    [the_internal_var2]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var2": "item3"
    })
    
    caller's vars to task (sub_task)::
    (*core.Cache)({
      "the_internal_var2": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 0,
      "the_internal_var": "item4"
    })
    
      located task-> 2 [sub_task]: 
    =Task2: [task ==> sub_task:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.loopitem}}",
          "name": "print"
        },
        {
          "name": "return",
          "cmd": {
            "the_internal_var2"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "the_internal_var2",
          Value: "{{.loopitem}}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item3",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    [local] dvar expanded result:
    {
      "the_internal_var2": "item4"
    }
    
    
    scope[local] merged: {
      "the_internal_var2": "item4",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "the_internal_var2": "item4",
      "loopitem": "item4",
      "loopindex": 3,
      "loopindex1": 4,
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    {{.loopitem}}
    ~~SubStep1: [print:  ]
    item4
    [the_internal_var2]
    ~~SubStep2: [return:  ]
    contextual return vars:
    
    (*core.Cache)({
      "the_internal_var2": "item4"
    })
    
    loop util conditional break
    
    -Step6:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "exec_vars"
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
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4",
      "the_internal_var2": "item4"
    })
    
    [exec_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "the_internal_var2": "item4",
      "up_runtime_task_layer_number": 1,
      "the_internal_var": "item4"
    })
    
    
```

##### Logs with different verbose level
* [c0181 log - verbose level v](../../logs/c0181_v)
* [c0181 log - verbose level vv](../../logs/c0181_vv)
* [c0181 log - verbose level vvv](../../logs/c0181_vvv)
* [c0181 log - verbose level vvvv](../../logs/c0181_vvvv)
* [c0181 log - verbose level vvvvv](../../logs/c0181_vvvvv)

##### References
* [Related Chapter](../../loop/c0181)
