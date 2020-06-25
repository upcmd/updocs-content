---
title: "c0034_vvvv"
date: 2020-06-25T01:55:42+66:00
draft: false
weight: 10343

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0034
                 Verbose -> vvvv
              ModuleName -> agitated_brown2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0034
    ---------group vars----------
    
    nonprod: {
      "c": "non-prod-c",
      "d": "non-prod-d",
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
      "b": "non-prod-b"
    }
    
    
    global: {
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
      }
    }
    
    
    groups members:[dev staging]
    module: [agitated_brown2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c",
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
      "d": "non-prod-d",
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
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
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
      "d": "non-prod-d",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "non-prod-a",
      "b": "non-prod-b",
      "c": "non-prod-c"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "show_school_details"
      },
      Dox: <nil>,
      Func: "call",
      Vars: {
        "a": "local-a",
        "b": "local-b"
      },
      Dvars: {
        {
          Name: "school",
          Value: "address:\n  state: NSW\n  city: sydney\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: LOCAL\n  school: {{.student.address.school}}\nprincipal: Mr Right\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "to_object"
          },
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
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
      "d": "non-prod-d",
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          }
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "local-a",
      "b": "local-b",
      "c": "non-prod-c"
    })
    
    agitated_brown2: overall final exec vars:
    
    (*core.Cache)({
      "b": "local-b",
      "c": "non-prod-c",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "d": "non-prod-d",
      "school_object": {
        "address": {
          "city": "sydney",
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "CBD": true,
            "name": "sydney"
          },
          "state": "NSW"
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "a": "local-a"
    })
    
      located task-> 2 [show_school_details]: 
    =Task2: [task ==> show_school_details:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.school -> {{.school}}\"\"\"",
        "echo \"\"\"2.school object CBD -> {{.school_object.address.suburb.CBD}}\"\"\"",
        "echo \"\"\"3.school object-> {{.school_object.address.school}}\"\"\"",
        "echo \"\"\"4.school object-> {{.school_object.principal}}\"\"\"",
        "echo \"\"\"5.a {{.a}}\"\"\"",
        "echo \"\"\"6.b {{.b}}\"\"\"",
        "echo \"\"\"7.school object-> {{.school_object|printobj}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "a": "show-school-details-a",
        "b": "show-school-details-b"
      },
      Dvars: {
        {
          Name: "class_room",
          Value: "3K",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "school",
          Value: "address:\n  suburb:\n    name: {{.student.address.suburb.name}}\n    postcode: 2000\n    CBD: no\n  school: {{.student.address.school}}\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
          Desc: "",
          Expand: 0,
          Flags: {
            "to_object"
          },
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "local-a",
      "b": "local-b",
      "up_runtime_task_layer_number": 1,
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "CBD": true
          },
          "state": "NSW",
          "city": "sydney"
        }
      },
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "c": "non-prod-c",
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
      "d": "non-prod-d"
    })
    
    agitated_brown2: overall final exec vars:
    
    (*core.Cache)({
      "school": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: no\n  school: Sydney Grammar\nprincipal: Mr Peter\nsomething: ref task does not have this field\n",
      "c": "non-prod-c",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "b": "local-b",
      "class_room": "3K",
      "d": "non-prod-d",
      "a": "local-a",
      "up_runtime_task_layer_number": 1,
      "school_object": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "state": "NSW",
          "city": "sydney"
        },
        "principal": "Mr Peter",
        "something": "ref task does not have this field"
      }
    })
    
    cmd( 1):
    echo """1.school -> {{.school}}"""
    
     \_ echo """1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
    """
    1.school -> address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: no
      school: Sydney Grammar
    principal: Mr Peter
    something: ref task does not have this field
     .. ok
    cmd( 2):
    echo """2.school object CBD -> {{.school_object.address.suburb.CBD}}"""
    
     \_ echo """2.school object CBD -> true"""
    2.school object CBD -> true
     .. ok
    cmd( 3):
    echo """3.school object-> {{.school_object.address.school}}"""
    
     \_ echo """3.school object-> Sydney Grammar"""
    3.school object-> Sydney Grammar
     .. ok
    cmd( 4):
    echo """4.school object-> {{.school_object.principal}}"""
    
     \_ echo """4.school object-> Mr Peter"""
    4.school object-> Mr Peter
     .. ok
    cmd( 5):
    echo """5.a {{.a}}"""
    
     \_ echo """5.a local-a"""
    5.a local-a
     .. ok
    cmd( 6):
    echo """6.b {{.b}}"""
    
     \_ echo """6.b local-b"""
    6.b local-b
     .. ok
    cmd( 7):
    echo """7.school object-> {{.school_object|printobj}}"""
    
    {
      "something": "ref task does not have this field",
      "address": {
        "state": "NSW",
        "city": "sydney",
        "school": "Sydney Grammar",
        "suburb": {
          "name": "sydney",
          "postcode": 2000,
          "CBD": true
        }
      },
      "principal": "Mr Peter"
    }
    
     \_ echo """7.school object-> {
      "address": {
        "suburb": {
          "postcode": 2000,
          "CBD": true,
          "name": "sydney"
        },
        "state": "NSW",
        "city": "sydney",
        "school": "Sydney Grammar"
      },
      "principal": "Mr Peter",
      "something": "ref task does not have this field"
    }
    
    """
    7.school object-> {
      address: {
        suburb: {
          postcode: 2000,
          CBD: true,
          name: sydney
        },
        state: NSW,
        city: sydney,
        school: Sydney Grammar
      },
      principal: Mr Peter,
      something: ref task does not have this field
    }
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0034 log - verbose level v](../../logs/c0034_v)
* [c0034 log - verbose level vv](../../logs/c0034_vv)
* [c0034 log - verbose level vvv](../../logs/c0034_vvv)
* [c0034 log - verbose level vvvv](../../logs/c0034_vvvv)
* [c0034 log - verbose level vvvvv](../../logs/c0034_vvvvv)

##### References
* [Related Chapter](../../dvars/c0034)
