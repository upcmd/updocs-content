---
title: "c0032_vvvvv"
date: 2020-09-18T00:51:24+99:00
draft: false
weight: 10324

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0032
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
    loading [Task]:  ./tests/functests/c0032
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0000c2820)((len=3 cap=3) {
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
      Dvars: (impl.Dvars) <nil>
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
       (string) (len=1) "a": (string) (len=10) "non-prod-a",
       (string) (len=1) "b": (string) (len=10) "non-prod-b",
       (string) (len=1) "c": (string) (len=10) "non-prod-c",
       (string) (len=1) "d": (string) (len=10) "non-prod-d"
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
      Name: (string) (len=3) "dev",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=1) "a": (string) (len=5) "dev-a",
       (string) (len=1) "b": (string) (len=5) "dev-b"
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
     }
    })
    
    [global] dvar expanded result:
    {
    }
    
    
    scope[global] merged: {
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
      }
    }
    
    
    [nonprod] dvar expanded result:
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "school_object": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    scope[nonprod] merged: {
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "non-prod-a",
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
    
    
    ---------group vars----------
    
    nonprod: {
      "a": "non-prod-a",
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
      "b": "non-prod-b",
      "c": "non-prod-c",
      "d": "non-prod-d"
    }
    
    
    global: {
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
      }
    }
    
    
    groups members:[dev staging]
    [dev] dvar expanded result:
    {
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
    
    
    scope[dev] merged: {
      "b": "dev-b",
      "a": "dev-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "school_object": {
        "principal": "Mr Peter",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": false
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    
    merged[ dev ] runtime vars:
    {
      "d": "non-prod-d",
      "a": "dev-a",
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
      },
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
      "b": "dev-b",
      "c": "non-prod-c"
    }
    
    (core.Cache) (len=7) {
     (string) (len=1) "d": (string) (len=10) "non-prod-d",
     (string) (len=1) "a": (string) (len=5) "dev-a",
     (string) (len=6) "school": (string) (len=112) "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
     (string) (len=13) "school_object": (map[interface {}]interface {}) (len=2) {
      (string) (len=7) "address": (map[interface {}]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[interface {}]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "CBD": (bool) false
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=9) "principal": (string) (len=8) "Mr Peter"
     },
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
     },
     (string) (len=1) "b": (string) (len=5) "dev-b",
     (string) (len=1) "c": (string) (len=10) "non-prod-c"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
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
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
      "b": "dev-b",
      "c": "non-prod-c",
      "d": "non-prod-d",
      "a": "dev-a",
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\n"
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
    """
    -
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    
    
    -
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
    echo """2.school object-> false"""
    -
    2.school object-> false
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=34) "echo \"\"\"2.school object-> false\"\"\"",
     Code: (int) 0,
     Output: (string) (len=23) "2.school object-> false",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
    cmd=>:
    echo """3.school object-> Sydney Grammar"""
    -
    3.school object-> Sydney Grammar
    
    -
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
    echo """4.school object-> Mr Peter"""
    -
    4.school object-> Mr Peter
    
    -
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
* [c0032 log - verbose level v](../../logs/c0032_v)
* [c0032 log - verbose level vv](../../logs/c0032_vv)
* [c0032 log - verbose level vvv](../../logs/c0032_vvv)
* [c0032 log - verbose level vvvv](../../logs/c0032_vvvv)
* [c0032 log - verbose level vvvvv](../../logs/c0032_vvvvv)

##### References
* [Related Chapter](../../dvars/c0032)
