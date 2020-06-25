---
title: "c0051_vvvv"
date: 2020-06-25T01:55:45+66:00
draft: false
weight: 10513

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
                 Verbose -> vvvv
              ModuleName -> serene_yonath1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0051
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
    module: [serene_yonath1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "bank_acct": "1234-5678",
      "enc_key": "my_non_enc_key"
    }
    
    dvar> bank_password_encrypted:
    "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw="
    
    dvar> bank_password_decrypted:
    "mybankpassword"
    
    dvar> bank_password:
    "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    
    dvar> bank_password_using_defause_config:
    "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    
    -------runtime global final merged with dvars-------
    
    {
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
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
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    })
    
    serene_yonath1: overall final exec vars:
    
    (*core.Cache)({
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678",
      "secure_bank_password": "mybankpassword"
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
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "up_runtime_task_layer_number": 1,
      "secure_bank_password": "mybankpassword",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "secure_bank_password_using_defause_config": "mybankpassword",
      "bank_password_encrypted": "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=",
      "enc_key": "my_non_enc_key",
      "bank_acct": "1234-5678"
    })
    
    serene_yonath1: overall final exec vars:
    
    (*core.Cache)({
      "secure_bank_password_using_defause_config": "mybankpassword",
      "up_runtime_task_layer_number": 1,
      "enc_key": "my_non_enc_key",
      "secure_bank_password": "mybankpassword",
      "bank_password_encrypted": "u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=",
      "bank_password_decrypted": "mybankpassword",
      "bank_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "bank_acct": "1234-5678",
      "bank_password_using_defause_config": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    })
    
    cmd( 1):
    echo "bank account  [{{.bank_acct}}]"
    
     \_ echo "bank account  [1234-5678]"
    bank account  [1234-5678]
     .. ok
    cmd( 2):
    echo "bank password encrypted [{{.bank_password_encrypted}}]"
    
     \_ echo "bank password encrypted [u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=]"
    bank password encrypted [u8qufuJugb3N1dLgxrZtLsTnIy0ZQjbJ9SuwtNipPGw=]
     .. ok
    cmd( 3):
    echo "bank password [{{.bank_password}}]"
    
     \_ echo "bank password [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]"
    bank password [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]
     .. ok
    cmd( 4):
    echo "secure bank password [{{.secure_bank_password}}]"
    
     \_ echo "secure bank password [mybankpassword]"
    secure bank password [mybankpassword]
     .. ok
    cmd( 5):
    echo "bank password using default config [{{.bank_password_using_defause_config}}]"
    
     \_ echo "bank password using default config [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]"
    bank password using default config [6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=]
     .. ok
    cmd( 6):
    echo "secure bank password using default config [{{.secure_bank_password_using_defause_config}}]"
    
     \_ echo "secure bank password using default config [mybankpassword]"
    secure bank password using default config [mybankpassword]
     .. ok
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