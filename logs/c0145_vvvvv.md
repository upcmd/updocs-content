---
title: "c0145_vvvvv"
date: 2020-10-07T00:11:26+1010:00
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
    loading [Task]:  ./tests/functests/c0145
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf0a0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e8e8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: mock up test to test module.template rendering ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "src": "./tests/functests/d0145.template",
            "dest": "/tmp/mockup_doc.md",
            "datafile": "d0145_data.yml"
          },
          "name": "template",
          "desc": "render a template file to a file 1"
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
    date: 2020-10-06T23:42:21+1010:00
    draft: false
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "cat /tmp/mockup_doc.md",
     Code: (int) 0,
     Output: (string) (len=74) "title: \"HelloWorld example\"\ndate: 2020-10-06T23:42:21+1010:00\ndraft: false",
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
