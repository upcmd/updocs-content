---
title: "c0146_vvvvv"
date: 2020-06-25T01:56:07+66:00
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
              ModuleName -> compassionate_euclid5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0146
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed120)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [compassionate_euclid5] instance id: [dev]
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
            "src": "./tests/functests/d0145.template",
            "dest": "/tmp/mockup_doc.md"
          }
        },
        {
          "cmd": {
            "{{eq .personname \"Tom Cruise\"}}",
            "{{eq .school \"james rules\"}}",
            "{{eq .title \"HelloWorld example\"}}"
          },
          "name": "assert"
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
    (core.Cache) (len=3) {
     (string) (len=10) "personname": (string) (len=9) "Tom Hanks",
     (string) (len=6) "folder": (string) (len=6) "module",
     (string) (len=5) "title": (string) (len=18) "HelloWorld example"
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "personname": "Tom Cruise",
      "folder": "module",
      "title": "HelloWorld example",
      "school": "james rules"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "james rules",
      "personname": "Tom Cruise",
      "folder": "module",
      "title": "HelloWorld example"
    }
    
    
    compassionate_euclid5: overall final exec vars:
    
    (*core.Cache)({
      "school": "james rules",
      "personname": "Tom Cruise",
      "folder": "module",
      "title": "HelloWorld example"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars](*core.Cache)({
      "school": "james rules",
      "personname": "Tom Cruise",
      "folder": "module",
      "title": "HelloWorld example"
    })
    
     2: inspect[exec_base_vars]{
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    compassionate_euclid5: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    cat /tmp/mockup_doc.md
    
     \_ cat /tmp/mockup_doc.md
    title: "HelloWorld example"
    date: 2020-06-25T00:27:39+66:00
    draft: false
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=72) "title: \"HelloWorld example\"\ndate: 2020-06-25T00:27:39+66:00\ndraft: false",
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
