---
title: "c0197_vvvvv"
date: 2020-09-18T00:51:59+99:00
draft: false
weight: 11974

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0197
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0197
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000175060)(<nil>)
    
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
      Do: "echo \"\"\"normal env var: $ENV_BBB\"\"\"\necho \"\"\"expected decrypted secure env var: $ENV_AAA\"\"\"\necho \"\"\"normal secure var: {{.secure_ENV_AAA}}\"\"\"\n",
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "enc_key": "my_enc_key"
      },
      Dvars: {
        {
          Name: "value_encrypted",
          Value: "{{ \"ENV_AAA\" | encryptAES .enc_key }}",
          Desc: "",
          Expand: 0,
          Flags: {
            "vvvv"
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
          Name: "ENV_BBB",
          Value: "I_AM_ENV_VAR_BBB",
          Desc: "",
          Expand: 0,
          Flags: {
            "envVar"
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
          Value: "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM=",
          Desc: "",
          Expand: 0,
          Flags: {
            "envVar",
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
      "enc_key": "my_enc_key"
    })
    
    dvar> value_encrypted:
    "vm1RckLUOmPJfbVzM2k4PcAgaBYc5rncOBkFqMU1s3w="
    
    -
    vm1RckLUOmPJfbVzM2k4PcAgaBYc5rncOBkFqMU1s3w=
    [local] dvar expanded result:
    {
      "ENV_BBB": "I_AM_ENV_VAR_BBB",
      "envVar_ENV_BBB": "I_AM_ENV_VAR_BBB",
      "ENV_AAA": "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM=",
      "secure_ENV_AAA": "ENV_AAA",
      "envVar_ENV_AAA": "ENV_AAA",
      "value_encrypted": "vm1RckLUOmPJfbVzM2k4PcAgaBYc5rncOBkFqMU1s3w="
    }
    
    
    scope[local] merged: {
      "secure_ENV_AAA": "ENV_AAA",
      "envVar_ENV_AAA": "ENV_AAA",
      "up_runtime_task_layer_number": 0,
      "enc_key": "my_enc_key",
      "value_encrypted": "vm1RckLUOmPJfbVzM2k4PcAgaBYc5rncOBkFqMU1s3w=",
      "ENV_BBB": "I_AM_ENV_VAR_BBB",
      "envVar_ENV_BBB": "I_AM_ENV_VAR_BBB",
      "ENV_AAA": "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM="
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "ENV_BBB": "I_AM_ENV_VAR_BBB",
      "envVar_ENV_BBB": "I_AM_ENV_VAR_BBB",
      "ENV_AAA": "tdRdCpkHCVz0xzzkthoPUsD6yS6w439zPMDNUot84mM=",
      "secure_ENV_AAA": "ENV_AAA",
      "envVar_ENV_AAA": "ENV_AAA",
      "up_runtime_task_layer_number": 0,
      "enc_key": "my_enc_key",
      "value_encrypted": "vm1RckLUOmPJfbVzM2k4PcAgaBYc5rncOBkFqMU1s3w="
    })
    
    cmd( 1):
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: {{.secure_ENV_AAA}}"""
    
    
    cmd=>:
    echo """normal env var: $ENV_BBB"""
    echo """expected decrypted secure env var: $ENV_AAA"""
    echo """normal secure var: ENV_AAA"""
    
    -
    normal env var: I_AM_ENV_VAR_BBB
    expected decrypted secure env var: ENV_AAA
    normal secure var: ENV_AAA
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=129) "echo \"\"\"normal env var: $ENV_BBB\"\"\"\necho \"\"\"expected decrypted secure env var: $ENV_AAA\"\"\"\necho \"\"\"normal secure var: ENV_AAA\"\"\"\n",
     Code: (int) 0,
     Output: (string) (len=102) "normal env var: I_AM_ENV_VAR_BBB\nexpected decrypted secure env var: ENV_AAA\nnormal secure var: ENV_AAA",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0197 log - verbose level v](../../logs/c0197_v)
* [c0197 log - verbose level vv](../../logs/c0197_vv)
* [c0197 log - verbose level vvv](../../logs/c0197_vvv)
* [c0197 log - verbose level vvvv](../../logs/c0197_vvvv)
* [c0197 log - verbose level vvvvv](../../logs/c0197_vvvvv)

##### References
* [Related Chapter](../../security/c0197)
