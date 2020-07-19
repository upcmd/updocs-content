---
title: "c0031_vvvvv"
date: 2020-07-20T02:01:34+77:00
draft: false
weight: 10314

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0031
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0031
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f74e0)((len=3 cap=3) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=1) {
       (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=3) "Tom",
        (string) (len=6) "gender": (string) (len=4) "Male",
        (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
         (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
          (string) (len=4) "name": (string) (len=6) "sydney",
          (string) (len=8) "postcode": (int) 2000,
          (string) (len=3) "CBD": (bool) true
         },
         (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
        }
       }
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=6) "school",
        Value: (string) (len=132) "address:\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: yes\n  school: {{.student.address.school}}\n",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=5) "toObj"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=3) "dev",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "c": (string) (len=10) "non-prod-c",
       (string) (len=1) "d": (string) (len=10) "non-prod-d",
       (string) (len=1) "a": (string) (len=10) "non-prod-a",
       (string) (len=1) "b": (string) (len=10) "non-prod-b"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=6) "school",
        Value: (string) (len=151) "address:\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: no\n  school: {{.student.address.school}}\nprincipal: Mr Peter\n",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=5) "toObj"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=3) "dev",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "b": (string) (len=5) "dev-b",
       (string) (len=1) "a": (string) (len=5) "dev-a"
      },
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [global] dvar expanded result:
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      }
    }
    
    
    scope[global] merged: {
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
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
    
    
    [nonprod] dvar expanded result:
    {
      "school_object": {
        "address": {
          "suburb": {
            "CBD": false,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    }
    
    
    scope[nonprod] merged: {
      "b": "non-prod-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          }
        },
        "principal": "Mr Peter"
      },
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a"
    }
    
    
    ---------group vars----------
    
    nonprod: {
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      }
    }
    
    
    global: {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
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
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    
    groups members:[dev staging]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    [dev] dvar expanded result:
    {
    }
    
    
    scope[dev] merged: {
      "b": "dev-b",
      "a": "dev-a"
    }
    
    
    merged[ dev ] runtime vars:
    {
      "a": "dev-a",
      "b": "dev-b",
      "c": "non-prod-c",
      "school_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        },
        "principal": "Mr Peter"
      },
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "d": "non-prod-d"
    }
    
    (core.Cache) (len=7) {
     (string) (len=13) "school_object": (map[interface {}]interface {}) (len=2) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true,
        (string) (len=4) "name": (string) (len=6) "sydney"
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=9) "principal": (string) (len=8) "Mr Peter"
     },
     (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male"
     },
     (string) (len=6) "school": (string) (len=112) "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
     (string) (len=1) "d": (string) (len=10) "non-prod-d",
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=1) "b": (string) (len=5) "dev-b",
     (string) (len=1) "c": (string) (len=10) "non-prod-c"
    }
    
    [runtime global] dvar expanded result:
    {
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      }
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "b": "dev-b",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "d": "non-prod-d",
      "a": "dev-a",
      "c": "non-prod-c",
      "school_object": {
        "principal": "Mr Peter",
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
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        },
        "name": "Tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school -> {{.school}}\"\"\"",
        "echo \"\"\"2.school object-> {{.school_object.address.suburb.CBD}}\"\"\"",
        "echo \"\"\"3.school object-> {{.school_object.address.school}}\"\"\"",
        "echo \"\"\"4.school object-> {{.school_object.principal}}\"\"\""
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
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "b": "dev-b",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "a": "dev-a",
      "c": "non-prod-c",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "principal": "Mr Peter"
      },
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "d": "non-prod-d",
      "school_object": {
        "principal": "Mr Peter",
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
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "dev-b",
      "a": "dev-a",
      "c": "non-prod-c"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "d": "non-prod-d",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "student": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "b": "dev-b",
      "sgp_address_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "a": "dev-a",
      "c": "non-prod-c",
      "school_object": {
        "principal": "Mr Peter",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      }
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
    cmd=>:
    echo """1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    """<=
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=135) "echo \"\"\"1.school -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=123) "1.school -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """2.school object-> {{.school_object.address.suburb.CBD}}"""
    
    cmd=>:
    echo """2.school object-> true"""<=
    2.school object-> true
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=33) "echo \"\"\"2.school object-> true\"\"\"",
     Code: (int) 0,
     Output: (string) (len=22) "2.school object-> true",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
    cmd=>:
    echo """3.school object-> Sydney Grammar"""<=
    3.school object-> Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=43) "echo \"\"\"3.school object-> Sydney Grammar\"\"\"",
     Code: (int) 0,
     Output: (string) (len=32) "3.school object-> Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
    cmd=>:
    echo """4.school object-> Mr Peter"""<=
    4.school object-> Mr Peter
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=37) "echo \"\"\"4.school object-> Mr Peter\"\"\"",
     Code: (int) 0,
     Output: (string) (len=26) "4.school object-> Mr Peter",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0031 log - verbose level v](../../logs/c0031_v)
* [c0031 log - verbose level vv](../../logs/c0031_vv)
* [c0031 log - verbose level vvv](../../logs/c0031_vvv)
* [c0031 log - verbose level vvvv](../../logs/c0031_vvvv)
* [c0031 log - verbose level vvvvv](../../logs/c0031_vvvvv)

##### References
* [Related Chapter](../../dvars/c0031)
