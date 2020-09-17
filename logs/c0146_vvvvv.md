---
title: "c0146_vvvvv"
date: 2020-09-18T01:27:48+99:00
draft: false
weight: 11464

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0146
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c1200)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "desc": "the vars in caller after invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
        },
        {
          "name": "template",
          "desc": "render a template file to a file 1",
          "cmd": {
            "dest": "/tmp/mockup_doc.md",
            "src": "./tests/functests/d0145.template"
          }
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .personname \"Tom Cruise\"}}",
            "{{eq .school \"james rules\"}}",
            "{{eq .title \"HelloWorld example\"}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "personname": "Tom Cruise",
        "school": "james rules"
      },
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "d0146_data.yml",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    loading [varsfile]:  ./tests/functests/d0146_data.yml
    (core.Cache) (len=3) {
     (string) (len=10) "personname": (string) (len=9) "Tom Hanks",
     (string) (len=6) "folder": (string) (len=6) "module",
     (string) (len=5) "title": (string) (len=18) "HelloWorld example"
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "school": "james rules",
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "up_runtime_task_layer_number": 0,
      "folder": "module"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "personname": "Tom Cruise",
      "up_runtime_task_layer_number": 0,
      "folder": "module",
      "school": "james rules",
      "title": "HelloWorld example"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "up_runtime_task_layer_number": 0,
      "folder": "module",
      "school": "james rules"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "folder": "module",
      "school": "james rules",
      "title": "HelloWorld example",
      "personname": "Tom Cruise"
    })
    
     2: inspect[exec_base_vars]
    {
    }
    
    map[dest:/tmp/mockup_doc.md src:./tests/functests/d0145.template]
    ~SubStep2: [template: render a template file to a file 1 ]
    [{{eq .personname "Tom Cruise"}} {{eq .school "james rules"}} {{eq .title "HelloWorld example"}}]
    ~SubStep3: [assert:  ]
     1 ASSERT OK:     [{{eq .personname "Tom Cruise"}}]
     2 ASSERT OK:     [{{eq .school "james rules"}}]
     3 ASSERT OK:     [{{eq .title "HelloWorld example"}}]
    -Step2:
    {
      Name: "",
      Do: {
        "cat /tmp/mockup_doc.md"
      },
      Dox: <nil>,
      Func: "shell",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
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
    date: 2020-09-18T00:48:24+99:00
    draft: false
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "cat /tmp/mockup_doc.md",
     Code: (int) 0,
     Output: (string) (len=72) "title: \"HelloWorld example\"\ndate: 2020-09-18T00:48:24+99:00\ndraft: false",
     ErrMsg: (string) ""
    }
    
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
