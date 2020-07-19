---
title: "c0154_vvvvv"
date: 2020-07-20T02:01:56+77:00
draft: false
weight: 11544

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0154
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0154
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf4c0)(<nil>)
    
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
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    }
    
    (core.Cache) (len=3) {
     (string) (len=14) "sydney_grammar": (map[string]interface {}) (len=1) {
      (string) (len=7) "address": (string) (len=6) "sydney"
     },
     (string) (len=1) "a": (string) (len=3) "aaa",
     (string) (len=1) "b": (string) (len=3) "bbb"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: access a non-exist var will not cause error or panic while you render it
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.c}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "access a non-exist var will not cause error or panic while you render it\n",
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
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    {{.c}}
    ~SubStep1: [print:  ]
    None
    -Step2: [: however if you access a non exist child element, then it will result in a warning error
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.b.not_exist}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "however if you access a non exist child element, then it will result in a warning error\n",
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
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    {{.b.not_exist}}
    ~SubStep1: [print:  ]
          template rendering problem -> template: .:1:4: executing "." at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "if the sub element does not exist, eg school_name does not exit, then the query result will give the result of the closest element result, in this caes the parent value \"aaa\" will be return\n",
          "cmd": {
            "reg": "myschool",
            "path": "a.school_name"
          }
        },
        {
          "name": "query",
          "cmd": {
            "path": "sydney_grammar.address",
            "reg": "school_address"
          }
        },
        {
          "name": "pathExisted",
          "cmd": {
            "reg": "address_existed",
            "path": "sydney_grammar.address"
          }
        },
        {
          "name": "pathExisted",
          "desc": "the state will be rendered as <no value>, this will be treated as not exist\n",
          "cmd": {
            "path": "sydney_grammar.state",
            "reg": "state_existed"
          }
        },
        {
          "name": "pathExisted",
          "cmd": {
            "path": "b.not_exist",
            "reg": "varb_sub_element_existed"
          }
        },
        {
          "name": "print",
          "cmd": "sydney_grammar.address exist: {{.address_existed}}\nsydney_grammar.state exist: {{.state_existed}}\nvarb_sub_element_existed exist: {{.varb_sub_element_existed}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      }
    })
    
    map[path:a.school_name reg:myschool]
    ~SubStep1: [query: if the sub element does not exist, eg school_name does not exit, then the query result will give the result of the closest element result, in this caes the parent value "aaa" will be return
     ]
    (string) (len=11) "sub yml str"
    
    (string) (len=4) "aaa\n"
    
    map[path:sydney_grammar.address reg:school_address]
    ~SubStep2: [query:  ]
    (string) (len=11) "sub yml str"
    
    (string) (len=16) "address: sydney\n"
    
    map[path:sydney_grammar.address reg:address_existed]
    ~SubStep3: [pathExisted:  ]
    map[path:sydney_grammar.state reg:state_existed]
    ~SubStep4: [pathExisted: the state will be rendered as <no value>, this will be treated as not exist
     ]
    map[path:b.not_exist reg:varb_sub_element_existed]
    ~SubStep5: [pathExisted:  ]
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
    sydney_grammar.address exist: {{.address_existed}}
    sydney_grammar.state exist: {{.state_existed}}
    varb_sub_element_existed exist: {{.varb_sub_element_existed}}
    
    ~SubStep6: [print:  ]
    sydney_grammar.address exist: true
    sydney_grammar.state exist: false
    varb_sub_element_existed exist: false
    
    -Step4: [: test pathExisted in templating ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "sydney_grammar.address exist: {{ pathExisted \"sydney_grammar.address\" }}\nsydney_grammar.state exist: {{ pathExisted \"sydney_grammar.state\"}}\nvarb_sub_element_existed exist: {{ pathExisted \"b.not_exist\"}}\n{{ if pathExisted \"b.not_exist\"}}\nI am happy\n{{ else }}\nI am sad\n{{ end }}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "test pathExisted in templating",
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
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb",
      "myschool": (*string)("aaa")
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true
    })
    
    sydney_grammar.address exist: {{ pathExisted "sydney_grammar.address" }}
    sydney_grammar.state exist: {{ pathExisted "sydney_grammar.state"}}
    varb_sub_element_existed exist: {{ pathExisted "b.not_exist"}}
    {{ if pathExisted "b.not_exist"}}
    I am happy
    {{ else }}
    I am sad
    {{ end }}
    
    ~SubStep1: [print:  ]
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
    sydney_grammar.address exist: true
    sydney_grammar.state exist: false
    varb_sub_element_existed exist: false
    
    I am sad
    
    
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "exec_vars"
          }
        },
        {
          "cmd": {
            "{{pathExisted \"sydney_grammar.address\" }}"
          },
          "name": "assert"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "address_existed": true,
      "state_existed": false,
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney")
    })
    
    [exec_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false
    })
    
    [{{pathExisted "sydney_grammar.address" }}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{pathExisted "sydney_grammar.address" }}]
    
```

##### Logs with different verbose level
* [c0154 log - verbose level v](../../logs/c0154_v)
* [c0154 log - verbose level vv](../../logs/c0154_vv)
* [c0154 log - verbose level vvv](../../logs/c0154_vvv)
* [c0154 log - verbose level vvvv](../../logs/c0154_vvvv)
* [c0154 log - verbose level vvvvv](../../logs/c0154_vvvvv)

##### References
* [Related Chapter](../../vars/c0154)
