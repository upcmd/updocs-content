---
title: "c0078_vvvvv"
date: 2020-08-09T01:36:10+88:00
draft: false
weight: 10784

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0078
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0078
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00011c4e0)(<nil>)
    
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
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.school_name}}"
        },
        {
          "name": "print",
          "cmd": "{{.school_details}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "school_name": "sydney grammar",
        "school_address": "1 fox road, sydney, nsw 2000"
      },
      Dvars: {
        {
          Name: "school_details",
          Value: "{{.school_name}} : {{.school_address}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "reg"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_name": "sydney grammar"
    })
    
    [local] dvar expanded result:
    {
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    }
    
    
    scope[local] merged: {
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    })
    
    {{.school_name}}
    ~SubStep1: [print:  ]
    sydney grammar
    {{.school_details}}
    ~SubStep2: [print:  ]
    sydney grammar : 1 fox road, sydney, nsw 2000
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.school_address}}"
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
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school_details": "sydney grammar : 1 fox road, sydney, nsw 2000"
    })
    
    {{.school_address}}
    ~SubStep1: [print:  ]
    None
    
```

##### Logs with different verbose level
* [c0078 log - verbose level v](../../logs/c0078_v)
* [c0078 log - verbose level vv](../../logs/c0078_vv)
* [c0078 log - verbose level vvv](../../logs/c0078_vvv)
* [c0078 log - verbose level vvvv](../../logs/c0078_vvvv)
* [c0078 log - verbose level vvvvv](../../logs/c0078_vvvvv)

##### References
* [Related Chapter](../../dvars/c0078)
