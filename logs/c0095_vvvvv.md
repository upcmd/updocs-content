---
title: "c0095_vvvvv"
date: 2020-09-18T01:27:37+99:00
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
    (*impl.Scopes)(0xc000173060)(<nil>)
    
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
          "name": "toObj",
          "desc": "the key is pointing to a var name and use its content as yml content\n",
          "cmd": {
            "fromkey": "person_yml",
            "reg": "person_object"
          }
        },
        {
          "cmd": "person_object",
          "name": "printObj"
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
          "name": "toObj",
          "desc": "use src content directly",
          "cmd": {
            "src": "person:\n  name: {{.person}}\n  age: 53\n",
            "reg": "{{.name_to_reg}}"
          }
        },
        {
          "name": "printObj",
          "cmd": "{{.name_to_reg}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person_yml": "person:\n  name: tom\n  age: 23\n",
        "name_to_convert": "person_yml",
        "name_to_reg": "person_dyna_object",
        "person": "jason"
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
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason"
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
      "person": "jason",
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      },
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object"
    })
    
    person_object
    ~SubStep2: [printObj:  ]
    (string) (len=13) "person_object"
    
    object:
     person_object: {
      "person": {
        "age": 23,
        "name": "tom"
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
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      },
      "person_dyna_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      },
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason"
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
      "person_dyna_object": {
        "person": {
          "name": "jason",
          "age": 53
        }
      },
      "up_runtime_task_layer_number": 0,
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      }
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
