---
title: "c0202_vvvvv"
date: 2020-10-07T00:11:36+1010:00
draft: false
weight: 12024

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0202
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
    loading [Task]:  ./tests/functests/c0202
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c1440)((len=1 cap=1) {
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=1 cap=1) {
       (string) (len=3) "dev"
      },
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=7) "enc_key",
        Value: (string) (len=10) "my_enc_key",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=6) "secret"
        },
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
    
    [nonprod] dvar expanded result:
    {
      "enc_key": "my_enc_key"
    }
    
    
    scope[nonprod] merged: {
    }
    
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
    })
    
    
    global: (*core.Cache)({
    })
    
    
    groups members:[dev]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e998)({
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
          "cmd": "var: {{.ENV_AAA}}\ndecrypted secure var: {{.secure_ENV_AAA}}\n"
        },
        {
          "name": "inspect",
          "desc": "the vars in caller after invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars",
            "exec_base_env_vars_configured",
            "exec_env_vars_configured",
            "debug_vars"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "value_encrypted",
          Value: "{{ \"ENV_AAA\" | encrypteAesWithVault \"enc_key\" }}",
          Desc: "encrypteAesWithVault will use the encryption key named enc_key stored in vault to encrypt\nit falls back to the normal cached store to get the enc_key if it does not exist\n",
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
    "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI="
    
    -
    bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=
    [local] dvar expanded result:
    {
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "ENV_AAA": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "secure_ENV_AAA": "ENV_AAA"
    }
    
    
    scope[local] merged: {
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "ENV_AAA": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "secure_ENV_AAA": "ENV_AAA",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_AAA": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI="
    })
    
    var: {{.ENV_AAA}}
    decrypted secure var: {{.secure_ENV_AAA}}
    
    ~SubStep1: [print:  ]
    var: bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=
    decrypted secure var: ENV_AAA
    
    [exec_vars exec_base_vars exec_base_env_vars_configured exec_env_vars_configured debug_vars]
    ~SubStep2: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "ENV_AAA": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "up_runtime_task_layer_number": 0,
      "secure_ENV_AAA": "ENV_AAA",
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI="
    })
    
     2: inspect[exec_base_vars]
    {
    }
    
     3: inspect[exec_base_env_vars_configured]
     4: inspect[exec_env_vars_configured]
     5: inspect[debug_vars]
    -debug vars-
    "UpRunTimeVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    "RuntimeVarsAndDvarsMerged"
    (*core.Cache)({
    })
    
    "ExecbaseVars"
    (*core.Cache)({
    })
    
    "TaskVars"
    (*core.Cache)({
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI="
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "ENV_AAA": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI=",
      "up_runtime_task_layer_number": 0,
      "secure_ENV_AAA": "ENV_AAA",
      "value_encrypted": "bDX8OmM9uGGm/zgCe177TTXvgdP52hNvUGOycxAfJAI="
    })
    
    --
    
```

##### Logs with different verbose level
* [c0202 log - verbose level v](../../logs/c0202_v)
* [c0202 log - verbose level vv](../../logs/c0202_vv)
* [c0202 log - verbose level vvv](../../logs/c0202_vvv)
* [c0202 log - verbose level vvvv](../../logs/c0202_vvvv)
* [c0202 log - verbose level vvvvv](../../logs/c0202_vvvvv)

##### References
* [Related Chapter](../../security/c0202)
