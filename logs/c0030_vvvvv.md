---
title: "c0030_vvvvv"
date: 2020-07-01T15:34:24+77:00
draft: false
weight: 10304

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0030
                 Verbose -> vvvvv
              ModuleName -> lonely_feynman7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0030
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001d75e0)((len=4 cap=4) {
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
        Name: (string) (len=13) "school_global",
        Value: (string) "",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=9) "to_object"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) (len=16) "d0030_school.yml",
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
       (string) (len=1) "d": (string) (len=10) "non-prod-d",
       (string) (len=1) "a": (string) (len=10) "non-prod-a",
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=14) "school_nonprod",
        Value: (string) "",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=9) "to_object"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) (len=16) "d0030_school.yml",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=4) "prod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=1 cap=1) {
       (string) (len=4) "prod"
      },
      Vars: (core.Cache) (len=4) {
       (string) (len=1) "d": (string) (len=6) "prod-d",
       (string) (len=1) "a": (string) (len=6) "prod-a",
       (string) (len=1) "b": (string) (len=6) "prod-b",
       (string) (len=1) "c": (string) (len=6) "prod-c"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=11) "school_prod",
        Value: (string) "",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=9) "to_object"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) (len=16) "d0030_school.yml",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     },
     (impl.Scope) {
      Name: (string) (len=7) "staging",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "b": (string) (len=9) "staging-b",
       (string) (len=1) "a": (string) (len=9) "staging-a"
      },
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [global] dvar expanded result:
    {
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
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
    
    
    scope[global] merged: {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
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
    
    
    [nonprod] dvar expanded result:
    {
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod_object": {
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
    
    
    scope[nonprod] merged: {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d"
    }
    
    
    [prod] dvar expanded result:
    {
      "school_prod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_prod_object": {
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
    
    
    scope[prod] merged: {
      "a": "prod-a",
      "b": "prod-b",
      "c": "prod-c",
      "school_prod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_prod_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "prod-d"
    }
    
    
    ---------group vars----------
    
    nonprod: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "non-prod-a"
    }
    
    
    prod: {
      "b": "prod-b",
      "c": "prod-c",
      "school_prod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_prod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "prod-d",
      "a": "prod-a"
    }
    
    
    global: {
      "student": {
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom"
      },
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global_object": {
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
    
    
    groups members:[dev staging prod]
    module: [lonely_feynman7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "c": "non-prod-c",
      "b": "non-prod-b",
      "school_global_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "a": "non-prod-a"
    }
    
    (core.Cache) (len=9) {
     (string) (len=14) "school_nonprod": (string) (len=93) "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
     (string) (len=1) "c": (string) (len=10) "non-prod-c",
     (string) (len=7) "student": (map[interface {}]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       }
      }
     },
     (string) (len=13) "school_global": (string) (len=93) "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
     (string) (len=1) "d": (string) (len=10) "non-prod-d",
     (string) (len=1) "a": (string) (len=10) "non-prod-a",
     (string) (len=1) "b": (string) (len=10) "non-prod-b",
     (string) (len=20) "school_global_object": (map[interface {}]interface {}) (len=1) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      }
     },
     (string) (len=21) "school_nonprod_object": (map[interface {}]interface {}) (len=1) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      }
     }
    }
    
    [runtime global] dvar expanded result:
    {
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
      }
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "d": "non-prod-d",
      "school_global_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "c": "non-prod-c",
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
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school_global -> {{.school_global}}\"\"\" - echo \"\"\"2.school_global object -> {{.school_global_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"3.school_nonprod -> {{.school_nonprod}}\"\"\"",
        "echo \"\"\"4.school_nonprod object -> {{.school_nonprod_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"5.sgp address -> {{.sgp_address}}\"\"\"",
        "echo \"\"\"6.sgp address object -> {{.sgp_address_object.address.suburb.name}}\"\"\"",
        "echo \"\"\"7.school_prod -> {{.school_prod}}\"\"\"",
        "echo \"\"\"8.school_prod object -> {{.school_prod_object.address.suburb.name}}\"\"\""
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
      "c": "non-prod-c",
      "sgp_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "a": "non-prod-a",
      "d": "non-prod-d",
      "school_global_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_nonprod_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        }
      },
      "b": "non-prod-b",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "a": "non-prod-a",
      "d": "non-prod-d",
      "school_global_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "sgp_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    
    lonely_feynman7: overall final exec vars:
    
    (*core.Cache)({
      "sgp_address_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "sgp_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_global": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
      "d": "non-prod-d",
      "school_global_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "c": "non-prod-c",
      "school_nonprod_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "non-prod-b",
      "school_nonprod": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "student": {
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          }
        },
        "name": "Tom"
      }
    })
    
    cmd( 1):
    echo """1.school_global -> {{.school_global}}""" - echo """2.school_global object -> {{.school_global_object.address.suburb.name}}"""
    
     \_ echo """1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """ - echo """2.school_global object -> sydney"""
    1.school_global -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     - echo 2.school_global object -> sydney
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=152) "1.school_global -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n - echo 2.school_global object -> sydney",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """3.school_nonprod -> {{.school_nonprod}}"""
    
     \_ echo """3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    3.school_nonprod -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=112) "3.school_nonprod -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """4.school_nonprod object -> {{.school_nonprod_object.address.suburb.name}}"""
    
     \_ echo """4.school_nonprod object -> sydney"""
    4.school_nonprod object -> sydney
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=33) "4.school_nonprod object -> sydney",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo """5.sgp address -> {{.sgp_address}}"""
    
     \_ echo """5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    5.sgp address -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=109) "5.sgp address -> address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo """6.sgp address object -> {{.sgp_address_object.address.suburb.name}}"""
    
     \_ echo """6.sgp address object -> sydney"""
    6.sgp address object -> sydney
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=30) "6.sgp address object -> sydney",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo """7.school_prod -> {{.school_prod}}"""
    
     \_ echo """7.school_prod -> <no value>"""
    7.school_prod -> <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=27) "7.school_prod -> <no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo """8.school_prod object -> {{.school_prod_object.address.suburb.name}}"""
    
     \_ echo """8.school_prod object -> <no value>"""
    8.school_prod object -> <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=34) "8.school_prod object -> <no value>",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0030 log - verbose level v](../../logs/c0030_v)
* [c0030 log - verbose level vv](../../logs/c0030_vv)
* [c0030 log - verbose level vvv](../../logs/c0030_vvv)
* [c0030 log - verbose level vvvv](../../logs/c0030_vvvv)
* [c0030 log - verbose level vvvvv](../../logs/c0030_vvvvv)

##### References
* [Related Chapter](../../dvars/c0030)
