---
title: "c0201_vvvvv"
date: 2020-10-06T23:46:28+1010:00
draft: false
weight: 12014

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0201
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
    loading [Task]:  ./tests/functests/c0201
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000c840)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e110)({
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
          "cmd": "var: {{.ENV_AAA}}\ndecrypted secure var: {{.secure_ENV_AAA}}\n",
          "name": "print"
        },
        {
          "desc": "the vars in caller after invoking module task",
          "cmd": {
            "exec_vars",
            "exec_base_vars",
            "exec_base_env_vars_configured",
            "exec_env_vars_configured",
            "debug_vars"
          },
          "name": "inspect"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
    "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    
    -
    bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=
    [local] dvar expanded result:
    {
      "enc_key": "my_enc_key",
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "ENV_AAA": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "secure_ENV_AAA": "ENV_AAA"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "ENV_AAA": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "secure_ENV_AAA": "ENV_AAA"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "ENV_AAA": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    })
    
    var: {{.ENV_AAA}}
    decrypted secure var: {{.secure_ENV_AAA}}
    
    ~SubStep1: [print:  ]
    var: bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=
    decrypted secure var: ENV_AAA
    
    [exec_vars exec_base_vars exec_base_env_vars_configured exec_env_vars_configured debug_vars]
    ~SubStep2: [inspect: the vars in caller after invoking module task ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "secure_ENV_AAA": "ENV_AAA",
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "ENV_AAA": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
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
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    })
    
    "ExecContextVars"
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "ENV_AAA": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "secure_ENV_AAA": "ENV_AAA"
    })
    
    --
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "var: {{.ENV_BBB}}\ndecrypted secure var: {{.secure_ENV_BBB}}\n"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "ENV_BBB",
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
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    })
    
    [local] dvar expanded result:
    {
      "secure_ENV_BBB": "ENV_AAA",
      "ENV_BBB": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    }
    
    
    scope[local] merged: {
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "up_runtime_task_layer_number": 0,
      "ENV_BBB": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "secure_ENV_BBB": "ENV_AAA"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_BBB": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=",
      "up_runtime_task_layer_number": 0,
      "value_encrypted": "bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA="
    })
    
    var: {{.ENV_BBB}}
    decrypted secure var: {{.secure_ENV_BBB}}
    
    ~SubStep1: [print:  ]
    var: bmKq5VyA5ZViYvE919DHfIz7i/7DHRzLyOVGzR5ahbA=
    decrypted secure var: ENV_AAA
    
    
```

##### Logs with different verbose level
* [c0201 log - verbose level v](../../logs/c0201_v)
* [c0201 log - verbose level vv](../../logs/c0201_vv)
* [c0201 log - verbose level vvv](../../logs/c0201_vvv)
* [c0201 log - verbose level vvvv](../../logs/c0201_vvvv)
* [c0201 log - verbose level vvvvv](../../logs/c0201_vvvvv)

##### References
* [Related Chapter](../../security/c0201)
