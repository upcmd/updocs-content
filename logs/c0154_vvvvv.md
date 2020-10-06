---
title: "c0154_vvvvv"
date: 2020-10-06T23:46:20+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0154
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e5520)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    (*core.Cache)(0xc000126930)((len=3) {
     (string) (len=1) "a": (string) (len=3) "aaa",
     (string) (len=1) "b": (string) (len=3) "bbb",
     (string) (len=14) "sydney_grammar": (map[string]interface {}) (len=1) {
      (string) (len=7) "address": (string) (len=6) "sydney"
     }
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    access a non-exist var will not cause error or panic while you render it
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    {{.c}}
    ~SubStep1: [print:  ]
    None
    -Step2: [
    however if you access a non exist child element, then it will result in a warning error
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0,
      "a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    {{.b.not_exist}}
    ~SubStep1: [print:  ]
          template rendering -> template: .:1:4: executing "." at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "query",
          "desc": "if the sub element does not exist, eg school_name does not exit, then the query result will give the result of the closest element result, in this caes the parent value \"aaa\" will be return\n",
          "cmd": {
            "path": "a.school_name",
            "reg": "myschool"
          }
        },
        {
          "cmd": {
            "path": "sydney_grammar.address",
            "reg": "school_address"
          },
          "name": "query"
        },
        {
          "name": "pathExisted",
          "cmd": {
            "path": "sydney_grammar.address",
            "reg": "address_existed"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0,
      "a": "aaa",
      "b": "bbb"
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
          "cmd": "sydney_grammar.address exist: {{ pathExisted \"sydney_grammar.address\" }}\nsydney_grammar.state exist: {{ pathExisted \"sydney_grammar.state\"}}\nvarb_sub_element_existed exist: {{ pathExisted \"b.not_exist\"}}\n{{ if pathExisted \"b.not_exist\"}}\nI am happy\n{{ else }}\nI am sad\n{{ end }}\n",
          "name": "print"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "address_existed": true,
      "up_runtime_task_layer_number": 0,
      "school_address": (*string)("sydney"),
      "myschool": (*string)("aaa"),
      "b": "bbb",
      "state_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "varb_sub_element_existed": false,
      "a": "aaa"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "address_existed": true,
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0,
      "state_existed": false,
      "a": "aaa",
      "school_address": (*string)("sydney"),
      "varb_sub_element_existed": false
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0,
      "varb_sub_element_existed": false,
      "b": "bbb",
      "address_existed": true,
      "state_existed": false,
      "school_address": (*string)("sydney"),
      "a": "aaa",
      "myschool": (*string)("aaa")
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
          "cmd": {
            "exec_vars"
          },
          "name": "inspect"
        },
        {
          "name": "assert",
          "cmd": {
            "{{pathExisted \"sydney_grammar.address\" }}"
          }
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "a": "aaa",
      "myschool": (*string)("aaa"),
      "address_existed": true,
      "state_existed": false,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "varb_sub_element_existed": false,
      "school_address": (*string)("sydney")
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "varb_sub_element_existed": false,
      "a": "aaa",
      "state_existed": false,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0,
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "varb_sub_element_existed": false,
      "a": "aaa"
    })
    
    [exec_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "varb_sub_element_existed": false,
      "a": "aaa",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
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
