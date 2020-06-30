---
title: "c0088_vvvv"
date: 2020-07-01T15:34:32+77:00
draft: false
weight: 10883

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0088
                 Verbose -> vvvv
              ModuleName -> nostalgic_cori9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0088
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [nostalgic_cori9] instance id: [dev]
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
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: use dynamic dir instead of static ref dir ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"1.address -> \\n{{.sgp_address_dyna_dir}}\"\"\"",
        "echo \"\"\"1.address object-> \\n{{.sgp_address_dyna_dir_object}}\"\"\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "dynadir": "./tests/functests"
      },
      Dvars: {
        {
          Name: "sgp_address_dyna_dir",
          Value: "",
          Desc: "",
          Expand: 0,
          Flags: {
            "to_object",
            "vvvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "d0030_school.yml",
          RefDir: "{{.dynadir}}",
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
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "dynadir": "./tests/functests"
    })
    
    dvar> sgp_address_dyna_dir:
    "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    
    dvar> sgp_address_dyna_dir_object:
    {
      "address": {
        "suburb": {
          "name": "sydney",
          "postcode": 2000,
          "CBD": true
        },
        "school": "Sydney Grammar"
      }
    }
    
    nostalgic_cori9: overall final exec vars:
    
    (*core.Cache)({
      "sgp_address_dyna_dir": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_dyna_dir_object": {
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
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        }
      },
      "dynadir": "./tests/functests"
    })
    
    cmd( 1):
    echo """1.address -> \n{{.sgp_address_dyna_dir}}"""
    
     \_ echo """1.address -> \naddress:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    1.address -> \naddress:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
     .. ok
    cmd( 2):
    echo """1.address object-> \n{{.sgp_address_dyna_dir_object}}"""
    
     \_ echo """1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]"""
    1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0088 log - verbose level v](../../logs/c0088_v)
* [c0088 log - verbose level vv](../../logs/c0088_vv)
* [c0088 log - verbose level vvv](../../logs/c0088_vvv)
* [c0088 log - verbose level vvvv](../../logs/c0088_vvvv)
* [c0088 log - verbose level vvvvv](../../logs/c0088_vvvvv)

##### References
* [Related Chapter](../../dvars/c0088)
