---
title: "c0088_vvvvv"
date: 2020-09-18T00:51:35+99:00
draft: false
weight: 10884

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
    loading [Task]:  ./tests/functests/c0088
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00025b060)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      }
    }
    
    (core.Cache) (len=1) {
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
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
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
            "toObj",
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "dynadir": "./tests/functests",
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "up_runtime_task_layer_number": 0
    })
    
    dvar> sgp_address_dyna_dir:
    "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n"
    
    -
    address:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    
    dvar[object]> sgp_address_dyna_dir_object:
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
    
    [local] dvar expanded result:
    {
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
      }
    }
    
    
    scope[local] merged: {
      "dynadir": "./tests/functests",
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
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
      "up_runtime_task_layer_number": 0,
      "dynadir": "./tests/functests",
      "sgp_address_dyna_dir": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
      "sgp_address_dyna_dir_object": {
        "address": {
          "suburb": {
            "CBD": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        }
      }
    })
    
    cmd( 1):
    echo """1.address -> \n{{.sgp_address_dyna_dir}}"""
    
    cmd=>:
    echo """1.address -> \naddress:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    """
    -
    1.address -> \naddress:
      suburb:
        name: sydney
        postcode: 2000
        CBD: yes
      school: Sydney Grammar
    
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=119) "echo \"\"\"1.address -> \\naddress:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n\"\"\"",
     Code: (int) 0,
     Output: (string) (len=107) "1.address -> \\naddress:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """1.address object-> \n{{.sgp_address_dyna_dir_object}}"""
    
    cmd=>:
    echo """1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]"""
    -
    1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=118) "echo \"\"\"1.address object-> \\nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]\"\"\"",
     Code: (int) 0,
     Output: (string) (len=107) "1.address object-> \\nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]",
     ErrMsg: (string) ""
    }
    
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
