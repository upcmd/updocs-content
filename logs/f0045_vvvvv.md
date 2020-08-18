---
title: "f0045_vvvvv"
date: 2020-08-18T15:16:27+88:00
draft: false
weight: 10454

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> f0045
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
    loading [Task]:  ./tests/functests/f0045
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001d6f20)((len=1 cap=1) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=12) "student_name",
        Value: (string) (len=68) "{{ env \"STUDENT_NAME\" |validateMandatoryFailIfNone \"student_name\" }}",
        Desc: (string) (len=72) "show that if required ENV var is empty and it will fail if this is empty",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     }
    })
    
          template rendering -> template: .:1:23: executing "." at <validateMandatoryFailIfNone "student_name">: error calling validateMandatoryFailIfNone:   ERROR: validateMandatoryFailIfNone [Required var:(student_name) must not be empty, please fix it]
    
    WARN:
        1:{{ env "STUDENT_NAME" |validateMandatoryFailIfNone "student_name" }}
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    -----trace for reference-----
    [global] dvar expanded result:
    {
      "student_name": "None"
    }
    
    
    scope[global] merged: {
      "student_name": "None"
    }
    
    
    ---------group vars----------
    
    global: {
      "student_name": "None"
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student_name": "None"
    }
    
    (core.Cache) (len=1) {
     (string) (len=12) "student_name": (string) (len=4) "None"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student_name": "None"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    
```

##### Logs with different verbose level
* [f0045 log - verbose level v](../../logs/f0045_v)
* [f0045 log - verbose level vv](../../logs/f0045_vv)
* [f0045 log - verbose level vvv](../../logs/f0045_vvv)
* [f0045 log - verbose level vvvv](../../logs/f0045_vvvv)
* [f0045 log - verbose level vvvvv](../../logs/f0045_vvvvv)

##### References
* [Related Chapter](../../env-vars/f0045)
