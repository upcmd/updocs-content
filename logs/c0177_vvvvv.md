---
title: "c0177_vvvvv"
date: 2020-08-18T15:16:25+88:00
draft: false
weight: 11774

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0177
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0177
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e6e60)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=6) "person": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "tom",
      (string) (len=3) "sex": (string) (len=4) "male",
      (string) (len=3) "age": (int) 18
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "person": {
        "sex": "male",
        "age": 18,
        "name": "tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: this is a story about tom
     ]
    Executing task stack layer: 1
    
    -Step1: [: tom is male
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "his age is {{.person.age}}\nhe is in school: {{.school}}\n",
          "cmd": "what gender is {{.person.name}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "school": "sydney grammar"
      },
      Dvars: <nil>,
      Desc: "{{.person.name}} is {{.person.sex}}\n",
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
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      },
      "school": "sydney grammar"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "person": {
        "age": 18,
        "name": "tom",
        "sex": "male"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "person": {
        "name": "tom",
        "sex": "male",
        "age": 18
      },
      "school": "sydney grammar"
    })
    
    what gender is {{.person.name}}
    ~SubStep1: [print: his age is 18
    he is in school: sydney grammar
     ]
    what gender is tom
    
```

##### Logs with different verbose level
* [c0177 log - verbose level v](../../logs/c0177_v)
* [c0177 log - verbose level vv](../../logs/c0177_vv)
* [c0177 log - verbose level vvv](../../logs/c0177_vvv)
* [c0177 log - verbose level vvvv](../../logs/c0177_vvvv)
* [c0177 log - verbose level vvvvv](../../logs/c0177_vvvvv)

##### References
* [Related Chapter](../../vars/c0177)
