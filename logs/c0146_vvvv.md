---
title: "c0146_vvvv"
date: 2020-10-07T00:11:26+1010:00
draft: false
weight: 11463

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0146
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
    loading [Task]:  ./tests/functests/c0146
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
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    loading [varsfile]:  ./tests/functests/d0146_data.yml
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "folder": "module",
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "folder": "module",
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "folder": "module",
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules"
    })
    
     2: inspect[exec_base_vars]
    {
    }
    
    ~SubStep2: [template: render a template file to a file 1 ]
    ~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .personname "Tom Cruise"}}]
     2 ASSERT OK:     [{{eq .school "james rules"}}]
     3 ASSERT OK:     [{{eq .title "HelloWorld example"}}]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    cat /tmp/mockup_doc.md
    
    cmd=>:
    cat /tmp/mockup_doc.md
    -
    title: "HelloWorld example"
    date: 2020-10-06T23:42:22+1010:00
    draft: false
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0146 log - verbose level v](../../logs/c0146_v)
* [c0146 log - verbose level vv](../../logs/c0146_vv)
* [c0146 log - verbose level vvv](../../logs/c0146_vvv)
* [c0146 log - verbose level vvvv](../../logs/c0146_vvvv)
* [c0146 log - verbose level vvvvv](../../logs/c0146_vvvvv)

##### References
* [Related Chapter](../../vars/c0146)
