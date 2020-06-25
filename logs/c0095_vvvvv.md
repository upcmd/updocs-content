---
title: "c0095_vvvvv"
date: 2020-06-25T01:55:53+66:00
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
              ModuleName -> berserk_babbage8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0095
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001d5040)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [berserk_babbage8] instance id: [dev]
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
          "desc": "the key is pointing to a var name and use its content as yml content\n",
          "cmd": {
            "fromkey": "person_yml",
            "reg": "person_object"
          },
          "name": "to_object"
        },
        {
          "name": "printobj",
          "cmd": "person_object"
        },
        {
          "cmd": "my name is: {{.person_object.person.name}}",
          "name": "print"
        },
        {
          "name": "to_object",
          "cmd": {
            "fromkey": "{{.name_to_convert}}",
            "reg": "{{.name_to_reg}}"
          }
        },
        {
          "name": "printobj",
          "cmd": "{{.name_to_reg}}"
        },
        {
          "name": "to_object",
          "desc": "use src content directly",
          "cmd": {
            "src": "person:\n  name: {{.person}}\n  age: 53\n",
            "reg": "{{.name_to_reg}}"
          }
        },
        {
          "name": "printobj",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n"
    }
    
    
    berserk_babbage8: overall final exec vars:
    
    (*core.Cache)({
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n"
    })
    
    map[fromkey:person_yml reg:person_object]
    ~SubStep1: [to_object: the key is pointing to a var name and use its content as yml content
     ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "person_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      }
    })
    
    person_object
    ~SubStep2: [printobj:  ]
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
    ~SubStep4: [to_object:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_dyna_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "name_to_convert": "person_yml",
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "person_object": {
        "person": {
          "age": 23,
          "name": "tom"
        }
      },
      "person_dyna_object": {
        "person": {
          "name": "tom",
          "age": 23
        }
      }
    })
    
    {{.name_to_reg}}
    ~SubStep5: [printobj:  ]
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
    ~SubStep6: [to_object: use src content directly ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "": "person_dyna_object",
      "person:\n  name: jason\n  age: 53\n": "person_dyna_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
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
      "name_to_convert": "person_yml"
    })
    
    {{.name_to_reg}}
    ~SubStep7: [printobj:  ]
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
