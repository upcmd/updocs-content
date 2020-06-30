---
title: "c0145_vvvvv"
date: 2020-07-01T15:34:42+77:00
draft: false
weight: 11454

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0145
                 Verbose -> vvvvv
              ModuleName -> cocky_nobel2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0145
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c8fc0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cocky_nobel2] instance id: [dev]
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
          "name": "template",
          "desc": "render a template file to a file 1",
          "cmd": {
            "dest": "/tmp/mockup_doc.md",
            "datafile": "d0145_data.yml",
            "src": "./tests/functests/d0145.template"
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
    
    
    cocky_nobel2: overall final exec vars:
    
    (*core.Cache)({
    })
    
    map[datafile:d0145_data.yml dest:/tmp/mockup_doc.md src:./tests/functests/d0145.template]
    ~SubStep1: [template: render a template file to a file 1 ]
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
    
    
    cocky_nobel2: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    cat /tmp/mockup_doc.md
    
     \_ cat /tmp/mockup_doc.md
    title: "HelloWorld example"
    date: 2020-06-27T03:07:59+66:00
    draft: false
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=72) "title: \"HelloWorld example\"\ndate: 2020-06-27T03:07:59+66:00\ndraft: false",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0145 log - verbose level v](../../logs/c0145_v)
* [c0145 log - verbose level vv](../../logs/c0145_vv)
* [c0145 log - verbose level vvv](../../logs/c0145_vvv)
* [c0145 log - verbose level vvvv](../../logs/c0145_vvvv)
* [c0145 log - verbose level vvvvv](../../logs/c0145_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0145)
