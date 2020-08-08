---
title: "c0165_vvvvv"
date: 2020-08-09T01:36:25+88:00
draft: false
weight: 11654

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0165
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
    loading [Task]:  ./tests/functests/c0165
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7040)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "obj": {
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      },
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n"
    }
    
    (core.Cache) (len=2) {
     (string) (len=3) "yml": (string) (len=72) "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
     (string) (len=3) "obj": (map[string]interface {}) (len=1) {
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=2) {
        (string) (len=4) "name": (string) (len=10) "sydney CBD",
        (string) (len=8) "postcode": (int) 2000
       },
       (string) (len=6) "school": (string) (len=2) "SG"
      }
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "obj": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "name": "sydney CBD"
          },
          "school": "SG"
        }
      },
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.yml}}"
        },
        {
          "name": "print",
          "desc": "print string representation of obj",
          "cmd": "{{.yml | ymlToObj}}"
        },
        {
          "name": "printObj",
          "desc": "print object",
          "cmd": "this_is_an_obj"
        },
        {
          "cmd": "{{ .obj | toJson}}",
          "name": "print",
          "desc": "object to json text"
        },
        {
          "cmd": "{{.yml | ymlToObj|reg \"this_is_another_obj\"}}",
          "name": "print",
          "desc": "convert yml string to obj in print"
        },
        {
          "cmd": "{{.this_is_another_obj}}",
          "name": "print",
          "desc": "print this_is_another_obj"
        },
        {
          "desc": "object to json text then to obj using ymlToObj\nyml is a superset of json, so ymlToObj works for json\n",
          "cmd": "{{ .obj | toJson |ymlToObj}}",
          "name": "print"
        },
        {
          "name": "print",
          "desc": "object to json text\nthen to obj using ymlToObj\nthen to yml\n",
          "cmd": "{{ .obj | toJson |ymlToObj|objToYml}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "{{.yml | ymlToObj|reg \"this_is_an_obj\"}}",
          Desc: "convert yml string to obj",
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
      "obj": {
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      },
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n"
    })
    
    ymlToObj:
    (*map[interface {}]interface {})({
      "address": {
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        },
        "school": "SG"
      }
    })
    
    [local] dvar expanded result:
    {
      "this_is_an_obj": (*map[interface {}]interface {})({
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      })
    }
    
    
    scope[local] merged: {
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "this_is_an_obj": (*map[interface {}]interface {})({
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      }),
      "obj": {
        "address": {
          "school": "SG",
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          }
        }
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "obj": {
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      },
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "this_is_an_obj": (*map[interface {}]interface {})({
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      })
    })
    
    {{.yml}}
    ~SubStep1: [print:  ]
    address:
      suburb:
        name: sydney CBD
        postcode: 2000
      school: SG
    
    {{.yml | ymlToObj}}
    ~SubStep2: [print: print string representation of obj ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "address": {
        "suburb": {
          "postcode": 2000,
          "name": "sydney CBD"
        },
        "school": "SG"
      }
    })
    
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    this_is_an_obj
    ~SubStep3: [printObj: print object ]
    (string) (len=14) "this_is_an_obj"
    
    object:
     this_is_an_obj: (*map[interface {}]interface {})({
      "address": {
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        },
        "school": "SG"
      }
    })
    
    {{ .obj | toJson}}
    ~SubStep4: [print: object to json text ]
    {"address":{"school":"SG","suburb":{"name":"sydney CBD","postcode":2000}}}
    {{.yml | ymlToObj|reg "this_is_another_obj"}}
    ~SubStep5: [print: convert yml string to obj in print ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "address": {
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        },
        "school": "SG"
      }
    })
    
    address:
      school: SG
      suburb:
        name: sydney CBD
        postcode: 2000
    
    {{.this_is_another_obj}}
    ~SubStep6: [print: print this_is_another_obj ]
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    {{ .obj | toJson |ymlToObj}}
    ~SubStep7: [print: object to json text then to obj using ymlToObj
    yml is a superset of json, so ymlToObj works for json
     ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "address": {
        "school": "SG",
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        }
      }
    })
    
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    {{ .obj | toJson |ymlToObj|objToYml}}
    ~SubStep8: [print: object to json text
    then to obj using ymlToObj
    then to yml
     ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "address": {
        "school": "SG",
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        }
      }
    })
    
    objToYml:
    "address:\n  school: SG\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n"
    
    address:
      school: SG
      suburb:
        name: sydney CBD
        postcode: 2000
    
    
```

##### Logs with different verbose level
* [c0165 log - verbose level v](../../logs/c0165_v)
* [c0165 log - verbose level vv](../../logs/c0165_vv)
* [c0165 log - verbose level vvv](../../logs/c0165_vvv)
* [c0165 log - verbose level vvvv](../../logs/c0165_vvvv)
* [c0165 log - verbose level vvvvv](../../logs/c0165_vvvvv)

##### References
* [Related Chapter](../../template/c0165)
