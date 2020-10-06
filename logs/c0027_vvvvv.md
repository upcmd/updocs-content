---
title: "c0027_vvvvv"
date: 2020-10-06T23:45:55+1010:00
draft: false
weight: 10274

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0027
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
    loading [Task]:  ./tests/functests/c0027
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf400)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
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
      }
    })
    
    (*core.Cache)(0xc00000e990)((len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=3) "cbd": (bool) true,
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      }
     }
    })
    
    [runtime global] dvar expanded result:
    {
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          }
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
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
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
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
        "echo \"\"\"school address object {{.school_address_object.suburb.name}}\"\"\"",
        "echo \"\"\"school address object -> {{.school_address_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"tom - {{.tom}}\"\"\""
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        }
      },
      "tom": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "student": {
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        },
        "name": "Tom"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n",
      "school_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "tom": {
            "name": "Tom"
          },
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "tom": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
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
      "up_runtime_task_layer_number": 0,
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      }
    })
    
    cmd( 1):
    echo """a smart guy=>{{.a_smart_guy}}"""
    
    cmd=>:
    echo """a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
    """
    -
    a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
    
    
    -
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
    echo """postcode=>2000"""
    -
    postcode=>2000
    
    -
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
      tom:
        name: Tom
    """
    -
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
      tom:
        name: Tom
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=140) "echo \"\"\"school address address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=128) "school address address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n  tom:\n    name: Tom",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """this guy is in =>{{.a_smart_guy_object.school}} school"""
    
    cmd=>:
    echo """this guy is in =>Sydney Grammar school"""
    -
    this guy is in =>Sydney Grammar school
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=49) "echo \"\"\"this guy is in =>Sydney Grammar school\"\"\"",
     Code: (int) 0,
     Output: (string) (len=38) "this guy is in =>Sydney Grammar school",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo """school address object {{.school_address_object.suburb.name}}"""
    
    cmd=>:
    echo """school address object <no value>"""
    -
    school address object <no value>
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=43) "echo \"\"\"school address object <no value>\"\"\"",
     Code: (int) 0,
     Output: (string) (len=32) "school address object <no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo """school address object -> {{.school_address_object.address.suburb.name}}"""
    
    cmd=>:
    echo """school address object -> sydney"""
    -
    school address object -> sydney
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=42) "echo \"\"\"school address object -> sydney\"\"\"",
     Code: (int) 0,
     Output: (string) (len=31) "school address object -> sydney",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo """tom - {{.tom}}"""
    
    cmd=>:
    echo """tom - map[gender:Male name:Tom school:Sydney Grammar]"""
    -
    tom - map[gender:Male name:Tom school:Sydney Grammar]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=64) "echo \"\"\"tom - map[gender:Male name:Tom school:Sydney Grammar]\"\"\"",
     Code: (int) 0,
     Output: (string) (len=53) "tom - map[gender:Male name:Tom school:Sydney Grammar]",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0027 log - verbose level v](../../logs/c0027_v)
* [c0027 log - verbose level vv](../../logs/c0027_vv)
* [c0027 log - verbose level vvv](../../logs/c0027_vvv)
* [c0027 log - verbose level vvvv](../../logs/c0027_vvvv)
* [c0027 log - verbose level vvvvv](../../logs/c0027_vvvvv)

##### References
* [Related Chapter](../../dvars/c0027)
