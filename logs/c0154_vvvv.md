---
title: "c0154_vvvv"
date: 2020-07-20T02:01:56+77:00
draft: false
weight: 11543

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0154
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
    current exec runtime vars:
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    ~SubStep1: [print:  ]
    None
    -Step2: [: however if you access a non exist child element, then it will result in a warning error
     ]
    current exec runtime vars:
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    ~SubStep1: [print:  ]
          template rendering problem -> template: .:1:4: executing "." at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
    
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "b": "bbb"
    })
    
    ~SubStep1: [query: if the sub element does not exist, eg school_name does not exit, then the query result will give the result of the closest element result, in this caes the parent value "aaa" will be return
     ]
    ~SubStep2: [query:  ]
    ~SubStep3: [pathExisted:  ]
    ~SubStep4: [pathExisted: the state will be rendered as <no value>, this will be treated as not exist
     ]
    ~SubStep5: [pathExisted:  ]
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    -----trace for reference-----
    ~SubStep6: [print:  ]
    sydney_grammar.address exist: true
    sydney_grammar.state exist: false
    varb_sub_element_existed exist: false
    
    -Step4: [: test pathExisted in templating ]
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
    
    self: final context exec vars:
    
    (*core.Cache)({
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
    })
    
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
