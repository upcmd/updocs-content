---
title: "c0203_vvvvv"
date: 2020-10-06T23:46:29+1010:00
draft: false
weight: 12034

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0203
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
    loading [Task]:  ./tests/functests/c0203
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001770c0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b68e0)({
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
      Do: "echo \"hello, this is a secrt value: {{.secure_ENV_AAA}}\"",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "enc_key",
          Value: "my_enc_key",
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
        },
        {
          Name: "value_encrypted",
          Value: "{{ \"ENV_AAA\" | encryptAES .enc_key }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv",
            "taskScope"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "ENV_AAA",
          Value: "{{.value_encrypted}}",
          Desc: "",
          Expand: 0,
          Flags: {
            "secure"
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
    
    dvar> value_encrypted:
    "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU="
    
    -
    4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=
    [local] dvar expanded result:
    {
      "enc_key": "my_enc_key",
      "value_encrypted": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=",
      "ENV_AAA": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=",
      "secure_ENV_AAA": "ENV_AAA"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=",
      "ENV_AAA": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=",
      "secure_ENV_AAA": "ENV_AAA"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_AAA": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU=",
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "4x7yAgfTuVenKXFkO9kur0+EIxVNL+i0lQnuMnjfdjU="
    })
    
    cmd( 1):
    echo "hello, this is a secrt value: {{.secure_ENV_AAA}}"
    
    cmd=>:
    echo "hello, this is a secrt value: SECURE_SENSITIVE_INFO_MASKED"
    -
    hello, this is a secrt value: ENV_AAA
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "echo \"hello, this is a secrt value: ENV_AAA\"",
     Code: (int) 0,
     Output: (string) (len=37) "hello, this is a secrt value: ENV_AAA",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0203 log - verbose level v](../../logs/c0203_v)
* [c0203 log - verbose level vv](../../logs/c0203_vv)
* [c0203 log - verbose level vvv](../../logs/c0203_vvv)
* [c0203 log - verbose level vvvv](../../logs/c0203_vvvv)
* [c0203 log - verbose level vvvvv](../../logs/c0203_vvvvv)

##### References
* [Related Chapter](../../security/c0203)
