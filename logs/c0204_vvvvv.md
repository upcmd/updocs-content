---
title: "c0204_vvvvv"
date: 2020-10-06T23:46:29+1010:00
draft: false
weight: 12044

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0204
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
    loading [Task]:  ./tests/functests/c0204
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000174fe0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b68d8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "hello, this is a secrt value: {{.my_secret}}\nhello, this is a secrt value: {{ \"my_secret\" | fromVault}}\nhello, this is a secrt value: {{ \"a_secret_does_not_exist_in_vault\" | fromVault}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "my_secret",
          Value: "you_will_never_know",
          Desc: "",
          Expand: 0,
          Flags: {
            "secret"
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "my_secret": "you_will_never_know"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    hello, this is a secrt value: {{.my_secret}}
    hello, this is a secrt value: {{ "my_secret" | fromVault}}
    hello, this is a secrt value: {{ "a_secret_does_not_exist_in_vault" | fromVault}}
    ~SubStep1: [print:  ]
    hello, this is a secrt value: <no value>
    hello, this is a secrt value: you_will_never_know
    hello, this is a secrt value: NotExistInVault
    
```

##### Logs with different verbose level
* [c0204 log - verbose level v](../../logs/c0204_v)
* [c0204 log - verbose level vv](../../logs/c0204_vv)
* [c0204 log - verbose level vvv](../../logs/c0204_vvv)
* [c0204 log - verbose level vvvv](../../logs/c0204_vvvv)
* [c0204 log - verbose level vvvvv](../../logs/c0204_vvvvv)

##### References
* [Related Chapter](../../security/c0204)
