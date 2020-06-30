---
title: "c0051_vvvvv"
date: 2020-07-01T15:34:28+77:00
draft: false
weight: 10514

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0051
                 Verbose -> vvvvv
              ModuleName -> elegant_hypatia5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0051
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb560)((len=2 cap=2) {
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=3) "dev",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=1) {
       (string) (len=7) "enc_key": (string) (len=14) "my_non_enc_key"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=4) "prod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=1 cap=1) {
       (string) (len=4) "prod"
      },
      Vars: (core.Cache) (len=1) {
       (string) (len=7) "enc_key": (string) (len=15) "my_prod_enc_key"
      },
      Dvars: (impl.Dvars) <nil>
     }
    })
    
    [nonprod] dvar expanded result:
    {
    }
    
    
    scope[nonprod] merged: {
      "enc_key": "my_non_enc_key"
    }
    
    
    [prod] dvar expanded result:
    {
    }
    
    
    scope[prod] merged: {
      "enc_key": "my_prod_enc_key"
    }
    
    
    ---------group vars----------
    
    nonprod: {
      "enc_key": "my_non_enc_key"
    }
    
    
    prod: {
      "enc_key": "my_prod_enc_key"
    }
    
    
    global: {
    }
    
    
    groups members:[dev staging prod]
    module: [elegant_hypatia5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "bank_acct": "1234-5678",
      "enc_key": "my_non_enc_key"
    }
    
    (core.Cache) (len=2) {
     (string) (len=7) "enc_key": (string) (len=14) "my_non_enc_key",
     (string) (len=9) "bank_acct": (string) (len=9) "1234-5678"
    }
    
    dvar> bank_password_encrypted:
    "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM="
    
    dvar> bank_password_decrypted:
    "mybankpassword"
    
    dvar> bank_password:
    "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    
    dvar> bank_password_using_defause_config:
    "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    
    [runtime global] dvar expanded result:
    {
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_decrypted": "mybankpassword"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "bank_acct": "1234-5678",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_decrypted": "mybankpassword",
      "enc_key": "my_non_enc_key"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: "task_generate_password",
      Dox: <nil>,
      Func: "call",
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
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_decrypted": "mybankpassword",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_decrypted": "mybankpassword",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678"
    }
    
    
    elegant_hypatia5: overall final exec vars:
    
    (*core.Cache)({
      "bank_password_decrypted": "mybankpassword",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM="
    })
    
    caller's vars to task (task_generate_password)::
    (*core.Cache)({
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_decrypted": "mybankpassword"
    })
    
      located task-> 2 [task_generate_password]: 
    =Task2: [task ==> task_generate_password:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"bank account  [{{.bank_acct}}]\"",
        "echo \"bank password encrypted [{{.bank_password_encrypted}}]\"",
        "echo \"bank password [{{.bank_password}}]\"",
        "echo \"secure bank password [{{.secure_bank_password}}]\"",
        "echo \"bank password using default config [{{.bank_password_using_defause_config}}]\"",
        "echo \"secure bank password using default config [{{.secure_bank_password_using_defause_config}}]\""
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
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "secure_bank_password": "mybankpassword",
      "up_runtime_task_layer_number": 1,
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "enc_key": "my_non_enc_key",
      "bank_password_decrypted": "mybankpassword",
      "up_runtime_task_layer_number": 1,
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_acct": "1234-5678",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword"
    }
    
    
    elegant_hypatia5: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_acct": "1234-5678",
      "bank_password_encrypted": "o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=",
      "enc_key": "my_non_enc_key",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    })
    
    cmd( 1):
    echo "bank account  [{{.bank_acct}}]"
    
     \_ echo "bank account  [1234-5678]"
    bank account  [1234-5678]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=25) "bank account  [1234-5678]",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "bank password encrypted [{{.bank_password_encrypted}}]"
    
     \_ echo "bank password encrypted [o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=]"
    bank password encrypted [o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=70) "bank password encrypted [o3Y/HtpaGPSDDeqjklWWhwiOLQPk4lEsb3fx4gSAXVM=]",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "bank password [{{.bank_password}}]"
    
     \_ echo "bank password [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]"
    bank password [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=60) "bank password [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "secure bank password [{{.secure_bank_password}}]"
    
     \_ echo "secure bank password [mybankpassword]"
    secure bank password [mybankpassword]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=37) "secure bank password [mybankpassword]",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "bank password using default config [{{.bank_password_using_defause_config}}]"
    
     \_ echo "bank password using default config [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]"
    bank password using default config [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=81) "bank password using default config [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "secure bank password using default config [{{.secure_bank_password_using_defause_config}}]"
    
     \_ echo "secure bank password using default config [mybankpassword]"
    secure bank password using default config [mybankpassword]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=58) "secure bank password using default config [mybankpassword]",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0051 log - verbose level v](../../logs/c0051_v)
* [c0051 log - verbose level vv](../../logs/c0051_vv)
* [c0051 log - verbose level vvv](../../logs/c0051_vvv)
* [c0051 log - verbose level vvvv](../../logs/c0051_vvvv)
* [c0051 log - verbose level vvvvv](../../logs/c0051_vvvvv)

##### References
* [Related Chapter](../../security/c0051)
