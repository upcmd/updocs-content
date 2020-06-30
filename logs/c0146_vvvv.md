---
title: "c0146_vvvv"
date: 2020-07-01T15:34:42+77:00
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
              ModuleName -> high_tesla1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0146
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [high_tesla1] instance id: [dev]
    merged[ dev ] runtime vars:
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
            "src": "./tests/functests/d0145.template",
            "dest": "/tmp/mockup_doc.md"
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
      VarsFile: "d0146_data.yml"
    }
    
    loading [varsfile]:  ./tests/functests/d0146_data.yml
    current exec runtime vars:
    (*core.Cache)({
      "folder": "module",
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules"
    })
    
    high_tesla1: overall final exec vars:
    
    (*core.Cache)({
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules",
      "folder": "module"
    })
    
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "title": "HelloWorld example",
      "personname": "Tom Cruise",
      "school": "james rules",
      "folder": "module"
    })
    
     2: inspect[exec_base_vars]{
    }
    
    ~SubStep2: [template: render a template file to a file 1 ]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    high_tesla1: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    cat /tmp/mockup_doc.md
    
     \_ cat /tmp/mockup_doc.md
    title: "HelloWorld example"
    date: 2020-06-27T03:08:00+66:00
    draft: false
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
