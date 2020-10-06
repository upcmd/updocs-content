---
title: "c0156_vvvvv"
date: 2020-10-07T00:11:28+1010:00
draft: false
weight: 11564

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0156
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e53c0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    (*core.Cache)(0xc000126910)((len=1) {
     (string) (len=6) "school": (string) (len=75) "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
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
    {
      Name: "",
      Do: {
        {
          "desc": "Use a actual cmd to register a variable does not make sense, but it is doable.\nIt is not advised to do it this way\n",
          "cmd": "{{.school |reg \"myschool\"}}",
          "name": "print"
        },
        {
          "name": "print",
          "desc": "please note that myschool is only a string, but not an object\n",
          "cmd": "{{.myschool}}"
        },
        {
          "cmd": "{{.myschool | ymlToObj |objToYml}}",
          "name": "print",
          "desc": "please note that below result is only a string representation of the object\nany golang template result can only be string, but not a object\n"
        },
        {
          "name": "print",
          "desc": "now register the object to a named var myschool_object\n",
          "cmd": "{{.myschool | ymlToObj |reg \"myschool_object\"}}"
        },
        {
          "name": "print",
          "desc": "same as above, this will only print the string reprentation of the object\n",
          "cmd": "{{.myschool_object}}"
        },
        {
          "name": "printObj",
          "desc": "same as above, this will only print the string reprentation of the object\n",
          "cmd": "{{.myschool_object}}"
        },
        {
          "name": "printObj",
          "desc": "* IMPORTANT\nuse the object var name to refer to the object in register\n",
          "cmd": "myschool_object"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "1st solution: register object in any template rending\n",
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
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "up_runtime_task_layer_number": 0
    })
    
    {{.school |reg "myschool"}}
    ~SubStep1: [print: Use a actual cmd to register a variable does not make sense, but it is doable.
    It is not advised to do it this way
     ]
    |
      sg:
        name: sydney grammar
        state: nsw
        address: sydney
        postcode: 2000
    
    {{.myschool}}
    ~SubStep2: [print: please note that myschool is only a string, but not an object
     ]
    sg:
      name: sydney grammar
      state: nsw
      address: sydney
      postcode: 2000
    
    {{.myschool | ymlToObj |objToYml}}
    ~SubStep3: [print: please note that below result is only a string representation of the object
    any golang template result can only be string, but not a object
     ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "sg": {
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    })
    
    objToYml:
    "sg:\n  address: sydney\n  name: sydney grammar\n  postcode: 2000\n  state: nsw\n"
    
    sg:
      address: sydney
      name: sydney grammar
      postcode: 2000
      state: nsw
    
    {{.myschool | ymlToObj |reg "myschool_object"}}
    ~SubStep4: [print: now register the object to a named var myschool_object
     ]
    ymlToObj:
    (*map[interface {}]interface {})({
      "sg": {
        "postcode": 2000,
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney"
      }
    })
    
    sg:
      address: sydney
      name: sydney grammar
      postcode: 2000
      state: nsw
    
    {{.myschool_object}}
    ~SubStep5: [print: same as above, this will only print the string reprentation of the object
     ]
    map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]
    {{.myschool_object}}
    ~SubStep6: [printObj: same as above, this will only print the string reprentation of the object
     ]
    (string) (len=20) "{{.myschool_object}}"
    
    object:
     map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]: (interface {}) <nil>
    
    myschool_object
    ~SubStep7: [printObj: * IMPORTANT
    use the object var name to refer to the object in register
     ]
    (string) (len=15) "myschool_object"
    
    object:
     myschool_object: (*map[interface {}]interface {})({
      "sg": {
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000,
        "name": "sydney grammar"
      }
    })
    
    -Step2: [
    2nd solution:
    use dvar auto coversion
    ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.myschool2}}\n{{.myschool2_object}}\n"
        },
        {
          "name": "printObj",
          "cmd": "myschool2_object"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "myschool2",
          Value: "{{.school }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "toObj",
            "v"
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
      Desc: "2nd solution:\nuse dvar auto coversion\n",
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
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      }),
      "up_runtime_task_layer_number": 0
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
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney",
        "postcode": 2000
      }
    }
    
    [local] dvar expanded result:
    {
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "address": "sydney",
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw"
        }
      }
    }
    
    
    scope[local] merged: {
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      },
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }),
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      },
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      })
    })
    
    {{.myschool2}}
    {{.myschool2_object}}
    
    ~SubStep1: [print:  ]
    sg:
      name: sydney grammar
      state: nsw
      address: sydney
      postcode: 2000
    
    map[sg:map[address:sydney name:sydney grammar postcode:2000 state:nsw]]
    
    myschool2_object
    ~SubStep2: [printObj:  ]
    (string) (len=16) "myschool2_object"
    
    object:
     myschool2_object: {
      "sg": {
        "postcode": 2000,
        "name": "sydney grammar",
        "state": "nsw",
        "address": "sydney"
      }
    }
    
    -Step3: [
    3rd solution:
    use toObj cmd
    details: https://upcmd.netlify.app/cmd-func/c0095/
    ]
    {
      Name: "",
      Do: {
        {
          "name": "toObj",
          "cmd": {
            "fromkey": "school",
            "reg": "myschool3_object"
          }
        },
        {
          "cmd": "myschool3_object",
          "name": "printObj"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "3rd solution:\nuse toObj cmd\ndetails: https://upcmd.netlify.app/cmd-func/c0095/\n",
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
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      }),
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }),
      "up_runtime_task_layer_number": 0,
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "address": "sydney",
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw"
        }
      }),
      "up_runtime_task_layer_number": 0
    })
    
    map[fromkey:school reg:myschool3_object]
    ~SubStep1: [toObj:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }),
      "": "myschool3_object"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool_object": (*map[interface {}]interface {})({
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }),
      "up_runtime_task_layer_number": 0,
      "myschool3_object": {
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      }
    })
    
    myschool3_object
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
