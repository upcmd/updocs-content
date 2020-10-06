---
title: "c0154_vvvv"
date: 2020-10-06T23:46:20+1010:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0154
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
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [
    access a non-exist var will not cause error or panic while you render it
    ]
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      },
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [print:  ]
    None
    -Step2: [
    however if you access a non exist child element, then it will result in a warning error
    ]
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "b": "bbb",
      "up_runtime_task_layer_number": 0,
      "sydney_grammar": {
        "address": "sydney"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "up_runtime_task_layer_number": 0,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa"
    })
    
    ~SubStep1: [print:  ]
          template rendering -> template: .:1:4: executing "." at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "a": "aaa",
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "sydney_grammar": {
        "address": "sydney"
      }
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
    
    ~SubStep6: [print:  ]
    sydney_grammar.address exist: true
    sydney_grammar.state exist: false
    varb_sub_element_existed exist: false
    
    -Step4: [: test pathExisted in templating ]
    current exec runtime vars:
    (*core.Cache)({
      "varb_sub_element_existed": false,
      "up_runtime_task_layer_number": 0,
      "myschool": (*string)("aaa"),
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "school_address": (*string)("sydney"),
      "address_existed": true,
      "state_existed": false,
      "b": "bbb"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "state_existed": false,
      "up_runtime_task_layer_number": 0,
      "b": "bbb",
      "varb_sub_element_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "a": "aaa",
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "address_existed": true
    })
    
    ~SubStep1: [print:  ]
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
          element validating problem -> template: validator:1:4: executing "validator" at <.b.not_exist>: can't evaluate field not_exist in type interface {}
    WARN:
        1:{{.b.not_exist}}
    
    sydney_grammar.address exist: true
    sydney_grammar.state exist: false
    varb_sub_element_existed exist: false
    
    I am sad
    
    
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "b": "bbb",
      "address_existed": true,
      "state_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "varb_sub_element_existed": false,
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "up_runtime_task_layer_number": 0,
      "a": "aaa"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "b": "bbb",
      "myschool": (*string)("aaa"),
      "up_runtime_task_layer_number": 0,
      "sydney_grammar": {
        "address": "sydney"
      },
      "school_address": (*string)("sydney"),
      "varb_sub_element_existed": false,
      "a": "aaa",
      "address_existed": true,
      "state_existed": false
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "state_existed": false,
      "sydney_grammar": {
        "address": "sydney"
      },
      "myschool": (*string)("aaa"),
      "school_address": (*string)("sydney"),
      "up_runtime_task_layer_number": 0,
      "varb_sub_element_existed": false,
      "b": "bbb",
      "a": "aaa",
      "address_existed": true
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
