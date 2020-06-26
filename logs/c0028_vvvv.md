---
title: "c0028_vvvv"
date: 2020-06-27T03:09:17+66:00
draft: false
weight: 10283

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
                 Verbose -> vvvv
              ModuleName -> cocky_franklin2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0028
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cocky_franklin2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
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
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n",
      "a_smart_guy_object": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "school_address": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
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
      "a_smart_guy_object": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
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
      },
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
      "a_smart_guy": "name: Tom\ngender: Male\nschool: Sydney Grammar\n"
    })
    
    cocky_franklin2: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      },
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
    
     \_ echo """a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
    """
    a smart guy=>name: Tom
    gender: Male
    school: Sydney Grammar
     .. ok
    cmd( 2):
    echo """postcode=>{{.student.address.suburb.postcode}}"""
    
     \_ echo """postcode=>2000"""
    postcode=>2000
     .. ok
    cmd( 3):
    echo """school address {{.school_address}}"""
    
     \_ echo """school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    school address address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    cmd( 4):
    echo """this guy is in =>{{.a_smart_guy_object.school}} school"""
    
     \_ echo """this guy is in =>Sydney Grammar school"""
    this guy is in =>Sydney Grammar school
     .. ok
    cmd( 5):
    echo """wrong ref here {{.school_address_object.suburb.name}}"""
    
     \_ echo """wrong ref here <no value>"""
    wrong ref here <no value>
     .. ok
    cmd( 6):
    echo """school address object -> {{.school_address_object.address.suburb.name}}"""
    
     \_ echo """school address object -> sydney"""
    school address object -> sydney
     .. ok
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
