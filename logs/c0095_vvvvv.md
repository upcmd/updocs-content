---
title: "c0095_vvvvv"
date: 2020-10-07T00:11:16+1010:00
draft: false
weight: 10954

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0095
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
    loading [Task]:  ./tests/functests/c0095
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bd120)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e8e8)({
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
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "toObj",
          "desc": "the key is pointing to a var name and use its content as yml content\n",
          "cmd": {
            "fromkey": "person_yml",
            "reg": "person_object"
          }
        },
        {
          "name": "printObj",
          "cmd": "person_object"
        },
        {
          "name": "print",
          "cmd": "my name is: {{.person_object.person.name}}"
        },
        {
          "name": "toObj",
          "cmd": {
            "fromkey": "{{.name_to_convert}}",
            "reg": "{{.name_to_reg}}"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.name_to_reg}}"
        },
        {
          "desc": "use src content directly",
          "cmd": {
            "src": "person:\n  name: {{.person}}\n  age: 53\n",
            "reg": "{{.name_to_reg}}"
          },
          "name": "toObj"
        },
        {
          "name": "printObj",
          "cmd": "{{.name_to_reg}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "name_to_convert": "person_yml",
        "name_to_reg": "person_dyna_object",
        "person": "jason",
        "person_yml": "person:\n  name: tom\n  age: 23\n"
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
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "up_runtime_task_layer_number": 0,
      "name_to_reg": "person_dyna_object"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml"
    })
    
    map[fromkey:person_yml reg:person_object]
    ~SubStep1: [toObj: the key is pointing to a var name and use its content as yml content
     ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      },
      "up_runtime_task_layer_number": 0,
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml"
    })
    
    person_object
    ~SubStep2: [printObj:  ]
    (string) (len=13) "person_object"
    
    object:
     person_object: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    my name is: {{.person_object.person.name}}
    ~SubStep3: [print:  ]
    my name is: tom
    map[fromkey:{{.name_to_convert}} reg:{{.name_to_reg}}]
    ~SubStep4: [toObj:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_dyna_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "person_object": {
        "person": {
          "age": 23,
          "name": "tom"
        }
      },
      "person_dyna_object": {
        "person": {
          "age": 23,
          "name": "tom"
        }
      },
      "up_runtime_task_layer_number": 0,
      "name_to_reg": "person_dyna_object"
    })
    
    {{.name_to_reg}}
    ~SubStep5: [printObj:  ]
    (string) (len=16) "{{.name_to_reg}}"
    
    object:
     person_dyna_object: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    map[reg:{{.name_to_reg}} src:person:
      name: {{.person}}
      age: 53
    ]
    ~SubStep6: [toObj: use src content directly ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_dyna_object",
      "person:\n  name: jason\n  age: 53\n": "person_dyna_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      },
      "person_dyna_object": {
        "person": {
          "name": "jason",
          "age": 53
        }
      },
      "up_runtime_task_layer_number": 0,
      "name_to_reg": "person_dyna_object",
      "person": "jason"
    })
    
    {{.name_to_reg}}
    ~SubStep7: [printObj:  ]
    (string) (len=16) "{{.name_to_reg}}"
    
    object:
     person_dyna_object: {
      "person": {
        "name": "jason",
        "age": 53
      }
    }
    
    
```

##### Logs with different verbose level
* [c0095 log - verbose level v](../../logs/c0095_v)
* [c0095 log - verbose level vv](../../logs/c0095_vv)
* [c0095 log - verbose level vvv](../../logs/c0095_vvv)
* [c0095 log - verbose level vvvv](../../logs/c0095_vvvv)
* [c0095 log - verbose level vvvvv](../../logs/c0095_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0095)
