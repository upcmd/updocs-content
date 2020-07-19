---
title: "c0156_vvvvv"
date: 2020-07-20T02:01:57+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0156
    -------full vars in scopes------
    (*impl.Scopes)(0xc000173300)(<nil>)
    
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
    
    (core.Cache) (len=1) {
     (string) (len=6) "school": (string) (len=75) "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    [runtime global] dvar expanded result:
    {
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
          "name": "print",
          "desc": "please note that below result is only a string representation of the object\nany golang template result can only be string, but not a object\n",
          "cmd": "{{.myschool | ymlToObj |objToYml}}"
        },
        {
          "desc": "now register the object to a named var myschool_object\n",
          "cmd": "{{.myschool | ymlToObj |reg \"myschool_object\"}}",
          "name": "print"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
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
    None
    {{.myschool | ymlToObj |objToYml}}
    ~SubStep3: [print: please note that below result is only a string representation of the object
    any golang template result can only be string, but not a object
     ]
          template rendering problem -> template: .:1:14: executing "." at <ymlToObj>: invalid value; expected string
    WARN:
        1:{{.myschool | ymlToObj |objToYml}}
    
    -----trace for reference-----
    
    {{.myschool | ymlToObj |reg "myschool_object"}}
    ~SubStep4: [print: now register the object to a named var myschool_object
     ]
          template rendering problem -> template: .:1:14: executing "." at <ymlToObj>: invalid value; expected string
    WARN:
        1:{{.myschool | ymlToObj |reg "myschool_object"}}
    
    -----trace for reference-----
    
    {{.myschool_object}}
    ~SubStep5: [print: same as above, this will only print the string reprentation of the object
     ]
    None
    {{.myschool_object}}
    ~SubStep6: [printObj: same as above, this will only print the string reprentation of the object
     ]
    (string) (len=20) "{{.myschool_object}}"
    
    object:
     None: (interface {}) <nil>
    
    myschool_object
    ~SubStep7: [printObj: * IMPORTANT
    use the object var name to refer to the object in register
     ]
    (string) (len=15) "myschool_object"
    
    object:
     myschool_object: (interface {}) <nil>
    
    -Step2: [: 2nd solution:
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
          "cmd": "myschool2_object",
          "name": "printObj"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
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
    
    [local] dvar expanded result:
    {
      "myschool2": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool2_object": {
        "sg": {
          "postcode": 2000,
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney"
        }
      }
    }
    
    
    scope[local] merged: {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
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
        "address": "sydney",
        "postcode": 2000,
        "name": "sydney grammar",
        "state": "nsw"
      }
    }
    
    -Step3: [: 3rd solution:
    use toObj cmd
    details: https://upcmd.netlify.app/cmd-func/c0095/
     ]
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "fromkey": "school",
            "reg": "myschool3_object"
          },
          "name": "toObj"
        },
        {
          "name": "printObj",
          "cmd": "myschool3_object"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    map[fromkey:school reg:myschool3_object]
    ~SubStep1: [toObj:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "": "myschool3_object",
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "school": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool": "sg:\n  name: sydney grammar\n  state: nsw\n  address: sydney\n  postcode: 2000\n",
      "myschool3_object": {
        "sg": {
          "name": "sydney grammar",
          "state": "nsw",
          "address": "sydney",
          "postcode": 2000
        }
      }
    })
    
    myschool3_object
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
