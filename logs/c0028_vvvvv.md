---
title: "c0028_vvvvv"
date: 2020-07-20T02:01:34+77:00
draft: false
weight: 10284

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0028
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0028
    -------full vars in scopes------
    (*impl.Scopes)(0xc000228980)(<nil>)
    
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
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "cbd": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"a smart guy=>{{.a_smart_guy}}\"\"\"",
        "echo \"\"\"postcode=>{{.student.address.suburb.postcode}}\"\"\"",
        "echo \"\"\"school address {{.school_address}}\"\"\"",
        "echo \"\"\"this guy is in =>{{.a_smart_guy_object.school}} school\"\"\"",
        "echo \"\"\"wrong ref here {{.school_address_object.suburb.name}}\"\"\"",
        "echo \"\"\"school address object -> {{.school_address_object.address.suburb.name}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_address_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      }
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
    cmd=>:
    echo """a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
    """<=
    a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=70) "echo \"\"\"a smart guy=>name: Tom\ngender: Male\nschool: Sydney Grammar\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=58) "a smart guy=>name: Tom\ngender: Male\nschool: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """postcode=>{{.student.address.suburb.postcode}}"""
    
    cmd=>:
    echo """postcode=>2000"""<=
    postcode=>2000
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"\"\"postcode=>2000\"\"\"",
     Code: (int) 0,
     Output: (string) (len=14) "postcode=>2000",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """school address {{.school_address}}"""
    
    cmd=>:
    echo """school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """<=
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=119) "echo \"\"\"school address address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=107) "school address address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """this guy is in =>{{.a_smart_guy_object.school}} school"""
    
    cmd=>:
    echo """this guy is in =>Sydney Grammar school"""<=
    this guy is in =>Sydney Grammar school
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=49) "echo \"\"\"this guy is in =>Sydney Grammar school\"\"\"",
     Code: (int) 0,
     Output: (string) (len=38) "this guy is in =>Sydney Grammar school",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo """wrong ref here {{.school_address_object.suburb.name}}"""
    
    cmd=>:
    echo """wrong ref here <no value>"""<=
    wrong ref here <no value>
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=36) "echo \"\"\"wrong ref here <no value>\"\"\"",
     Code: (int) 0,
     Output: (string) (len=25) "wrong ref here <no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo """school address object -> {{.school_address_object.address.suburb.name}}"""
    
    cmd=>:
    echo """school address object -> sydney"""<=
    school address object -> sydney
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=42) "echo \"\"\"school address object -> sydney\"\"\"",
     Code: (int) 0,
     Output: (string) (len=31) "school address object -> sydney",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0028 log - verbose level v](../../logs/c0028_v)
* [c0028 log - verbose level vv](../../logs/c0028_vv)
* [c0028 log - verbose level vvv](../../logs/c0028_vvv)
* [c0028 log - verbose level vvvv](../../logs/c0028_vvvv)
* [c0028 log - verbose level vvvvv](../../logs/c0028_vvvvv)

##### References
* [Related Chapter](../../dvars/c0028)
