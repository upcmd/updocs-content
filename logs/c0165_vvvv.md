---
title: "c0165_vvvv"
date: 2020-09-18T01:27:51+99:00
draft: false
weight: 11653

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0165
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0165
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
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "obj": {
        "address": {
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          },
          "school": "SG"
        }
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "obj": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "name": "sydney CBD"
          },
          "school": "SG"
        }
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "obj": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "name": "sydney CBD"
          },
          "school": "SG"
        }
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "this_is_an_obj": (*map[interface {}]interface {})({
        "address": {
          "school": "SG",
          "suburb": {
            "name": "sydney CBD",
            "postcode": 2000
          }
        }
      }),
      "yml": "address:\n  suburb:\n    name: sydney CBD\n    postcode: 2000\n  school: SG\n",
      "obj": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "name": "sydney CBD"
          },
          "school": "SG"
        }
      }
    })
    
    ~SubStep1: [print:  ]
    address:
      suburb:
        name: sydney CBD
        postcode: 2000
      school: SG
    
    ~SubStep2: [print: print string representation of obj ]
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    ~SubStep3: [printObj: print object ]
    (string) (len=14) "this_is_an_obj"
    
    object:
     this_is_an_obj: (*map[interface {}]interface {})({
      "address": {
        "suburb": {
          "name": "sydney CBD",
          "postcode": 2000
        },
        "school": "SG"
      }
    })
    
    ~SubStep4: [print: object to json text ]
    {"address":{"school":"SG","suburb":{"name":"sydney CBD","postcode":2000}}}
    ~SubStep5: [print: convert yml string to obj in print ]
    address:
      school: SG
      suburb:
        name: sydney CBD
        postcode: 2000
    
    ~SubStep6: [print: print this_is_another_obj ]
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    ~SubStep7: [print: object to json text then to obj using ymlToObj
    yml is a superset of json, so ymlToObj works for json
     ]
    map[address:map[school:SG suburb:map[name:sydney CBD postcode:2000]]]
    ~SubStep8: [print: object to json text
    then to obj using ymlToObj
    then to yml
     ]
    address:
      school: SG
      suburb:
        name: sydney CBD
        postcode: 2000
    
    
```

##### Logs with different verbose level
* [c0165 log - verbose level v](../../logs/c0165_v)
* [c0165 log - verbose level vv](../../logs/c0165_vv)
* [c0165 log - verbose level vvv](../../logs/c0165_vvv)
* [c0165 log - verbose level vvvv](../../logs/c0165_vvvv)
* [c0165 log - verbose level vvvvv](../../logs/c0165_vvvvv)

##### References
* [Related Chapter](../../template/c0165)
