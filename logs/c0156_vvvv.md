---
title: "c0156_vvvv"
date: 2020-10-06T23:46:20+1010:00
draft: false
weight: 11563

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0156
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0156
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    1st solution: register object in any template rending
    ]
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    ~SubStep1: [print: Use a actual cmd to register a variable does not make sense, but it is doable.
    It is not advised to do it this way
     ]
    |
      sg:
        name: sydney grammar
        state: nsw
        address: sydney
        postcode: 2000
    
    ~SubStep2: [print: please note that myschool is only a string, but not an object
     ]
    sg:
      name: sydney grammar
      state: nsw
      address: sydney
      postcode: 2000
    
    ~SubStep3: [print: please note that below result is only a string representation of the object
    any golang template result can only be string, but not a object
     ]
    sg:
      address: sydney
      name: sydney grammar
      postcode: 2000
      state: nsw
    
    ~SubStep4: [print: now register the object to a named var myschool_object
     ]
    sg:
      address: sydney
      name: sydney grammar
      postcode: 2000
      state: nsw
    
    ~SubStep5: [print: same as above, this will only print the string reprentation of the object
     ]
    map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]
    ~SubStep6: [printObj: same as above, this will only print the string reprentation of the object
     ]
    (string) (len=20) "{{.myschool_object}}"
    
    object:
     map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]: (interface {}) <nil>
    
    ~SubStep7: [printObj: * IMPORTANT
    use the object var name to refer to the object in register
     ]
    (string) (len=15) "myschool_object"
    
    object:
     myschool_object: (*map[interface {}]interface {})({
      "sg": {
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    })
    
    -Step2: [
    2nd solution:
    use dvar auto coversion
    ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "address": "sydney",
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw"
        }
      }),
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    dvar> myschool2:
    "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    
    -
    sg:
      name: sydney grammar
      state: nsw
      address: sydney
      postcode: 2000
    
    dvar[object]> myschool2_object:
    {
      "sg": {
        "postcode": 2000,
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney"
      }
    }
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      },
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      }),
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    sg:
      name: sydney grammar
      state: nsw
      address: sydney
      postcode: 2000
    
    map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]
    
    ~SubStep2: [printObj:  ]
    (string) (len=16) "myschool2_object"
    
    object:
     myschool2_object: {
      "sg": {
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    }
    
    -Step3: [
    3rd solution:
    use toObj cmd
    details: https://upcmd.netlify.app/cmd-func/c0095/
    ]
    current exec runtime vars:
    (*core.Cache)({
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000,
          "name": "sydney grammar"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "address": "sydney",
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    ~SubStep1: [toObj:  ]
    ~SubStep2: [printObj:  ]
    (string) (len=16) "myschool3_object"
    
    object:
     myschool3_object: {
      "sg": {
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    }
    
    
```

##### Logs with different verbose level
* [c0156 log - verbose level v](../../logs/c0156_v)
* [c0156 log - verbose level vv](../../logs/c0156_vv)
* [c0156 log - verbose level vvv](../../logs/c0156_vvv)
* [c0156 log - verbose level vvvv](../../logs/c0156_vvvv)
* [c0156 log - verbose level vvvvv](../../logs/c0156_vvvvv)

##### References
* [Related Chapter](../../object-oriented/c0156)
