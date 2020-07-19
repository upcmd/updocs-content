---
title: "c0156_vvvv"
date: 2020-07-20T02:01:57+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0156
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: 1st solution: register object in any template rending
     ]
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
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
    None
    ~SubStep3: [print: please note that below result is only a string representation of the object
    any golang template result can only be string, but not a object
     ]
          template rendering problem -> template: .:1:14: executing "." at <ymlToObj>: invalid value; expected string
    WARN:
        1:{{.myschool | ymlToObj |objToYml}}
    
    -----trace for reference-----
    
    ~SubStep4: [print: now register the object to a named var myschool_object
     ]
          template rendering problem -> template: .:1:14: executing "." at <ymlToObj>: invalid value; expected string
    WARN:
        1:{{.myschool | ymlToObj |reg "myschool_object"}}
    
    -----trace for reference-----
    
    ~SubStep5: [print: same as above, this will only print the string reprentation of the object
     ]
    None
    ~SubStep6: [printObj: same as above, this will only print the string reprentation of the object
     ]
    (string) (len=20) "{{.myschool_object}}"
    
    object:
     None: (interface {}) <nil>
    
    ~SubStep7: [printObj: * IMPORTANT
    use the object var name to refer to the object in register
     ]
    (string) (len=15) "myschool_object"
    
    object:
     myschool_object: (interface {}) <nil>
    
    -Step2: [: 2nd solution:
    use dvar auto coversion
     ]
    current exec runtime vars:
    (*core.Cache)({
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    dvar> myschool2:
    "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    
    dvar> myschool2_object:
    {
      "sg": {
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    }
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }
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
    
    -Step3: [: 3rd solution:
    use toObj cmd
    details: https://upcmd.netlify.app/cmd-func/c0095/
     ]
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    ~SubStep1: [toObj:  ]
    ~SubStep2: [printObj:  ]
    (string) (len=16) "myschool3_object"
    
    object:
     myschool3_object: {
      "sg": {
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000,
        "name": "sydney grammar"
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
