---
title: "c0088_vvvv"
date: 2020-08-18T15:16:04+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0088
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
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
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: use dynamic dir instead of static ref dir ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
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
      "dynadir": "./tests/functests"
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
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sgp_address_dyna_dir": "address:\n  suburb:\n    name: sydney\n    postcode: 2000\n    CBD: yes\n  school: Sydney Grammar\n",
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
      "dynadir": "./tests/functests",
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
    cmd( 2):
    echo """1.address object-> \n{{.sgp_address_dyna_dir_object}}"""
    
    cmd=>:
    echo """1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]"""
    -
    1.address object-> \nmap[address:map[school:Sydney Grammar suburb:map[CBD:true name:sydney postcode:2000]]]
    -
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
