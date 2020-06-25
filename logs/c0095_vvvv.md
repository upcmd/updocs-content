---
title: "c0095_vvvv"
date: 2020-06-25T01:55:53+66:00
draft: false
weight: 10953

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
                 Verbose -> vvvv
              ModuleName -> stupefied_stallman9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0095
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [stupefied_stallman9] instance id: [dev]
    merged[ dev ] runtime vars:
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
          "cmd": {
            "reg": "person_object",
            "fromkey": "person_yml"
          },
          "name": "to_object",
          "desc": "the key is pointing to a var name and use its content as yml content\n"
        },
        {
          "name": "printobj",
          "cmd": "person_object"
        },
        {
          "name": "print",
          "cmd": "my name is: {{.person_object.person.name}}"
        },
        {
          "name": "to_object",
          "cmd": {
            "reg": "{{.name_to_reg}}",
            "fromkey": "{{.name_to_convert}}"
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
            "reg": "{{.name_to_reg}}",
            "src": "person:\n  name: {{.person}}\n  age: 53\n"
          }
        },
        {
          "cmd": "{{.name_to_reg}}",
          "name": "printobj"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "person": "jason",
        "person_yml": "person:\n  name: tom\n  age: 23\n",
        "name_to_convert": "person_yml",
        "name_to_reg": "person_dyna_object"
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
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml"
    })
    
    stupefied_stallman9: overall final exec vars:
    
    (*core.Cache)({
      "name_to_reg": "person_dyna_object",
      "person": "jason",
      "person_yml": "person:\n  name: tom\n  age: 23\n",
      "name_to_convert": "person_yml"
    })
    
    ~SubStep1: [to_object: the key is pointing to a var name and use its content as yml content
     ]
    ~SubStep2: [printobj:  ]
    (string) (len=13) "person_object"
    
    object:
     person_object: {
      "person": {
        "age": 23,
        "name": "tom"
      }
    }
    
    ~SubStep3: [print:  ]
    my name is: tom
    ~SubStep4: [to_object:  ]
    ~SubStep5: [printobj:  ]
    (string) (len=16) "{{.name_to_reg}}"
    
    object:
     person_dyna_object: {
      "person": {
        "name": "tom",
        "age": 23
      }
    }
    
    ~SubStep6: [to_object: use src content directly ]
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
