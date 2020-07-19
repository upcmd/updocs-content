---
title: "c0153_vvvvv"
date: 2020-07-20T02:01:56+77:00
draft: false
weight: 11534

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0153
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0153
    -------full vars in scopes------
    (*impl.Scopes)(0xc000177aa0)((len=6 cap=6) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=4) "port": (int) 5432,
       (string) (len=9) "db_driver": (string) (len=8) "postgres"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=16) "A_GLOBAL_ENV_VAR",
        Value: (string) (len=16) "a_global_env_var",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=6) "envVar"
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
     },
     (impl.Scope) {
      Name: (string) (len=7) "nonprod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=2 cap=2) {
       (string) (len=3) "dev",
       (string) (len=7) "staging"
      },
      Vars: (core.Cache) (len=4) {
       (string) (len=11) "db_password": (string) (len=34) "could_be_encrypted_using_upcmd_too",
       (string) (len=7) "db_host": (string) (len=26) "nonpord_database.test.host",
       (string) (len=7) "db_port": (int) 8354,
       (string) (len=7) "db_user": (string) (len=12) "test_db_user"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=11) "db_password",
        Value: (string) (len=44) "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
        Desc: (string) "",
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
     },
     (impl.Scope) {
      Name: (string) (len=4) "prod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) (len=1 cap=1) {
       (string) (len=4) "prod"
      },
      Vars: (core.Cache) (len=1) {
       (string) (len=10) "host_alias": (string) (len=4) "prod"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=3) "dev",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=1) {
       (string) (len=10) "host_alias": (string) (len=3) "dev"
      },
      Dvars: (impl.Dvars) (len=2 cap=2) {
       (impl.Dvar) {
        Name: (string) (len=7) "db_host",
        Value: (string) (len=57) "{{ env \"DB_HOST\" |default \"nonpord_database.test.host\" }}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       },
       (impl.Dvar) {
        Name: (string) (len=13) "A_DEV_ENV_VAR",
        Value: (string) (len=68) "{{ env \"A_GLOBAL_ENV_VAR\" |default \"A_GLOBAL_ENV_VAR_NOT_LOCATED\" }}",
        Desc: (string) "",
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
     },
     (impl.Scope) {
      Name: (string) (len=7) "staging",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=1) {
       (string) (len=10) "host_alias": (string) (len=7) "staging"
      },
      Dvars: (impl.Dvars) <nil>
     },
     (impl.Scope) {
      Name: (string) (len=4) "prod",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=3) {
       (string) (len=7) "db_host": (string) (len=25) "pord_database.proddb.host",
       (string) (len=7) "db_user": (string) (len=12) "prod_db_user",
       (string) (len=10) "host_alias": (string) (len=4) "prod"
      },
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=11) "db_password",
        Value: (string) (len=17) "prod_encrypte_aes",
        Desc: (string) "",
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
    
    [global] dvar expanded result:
    {
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var"
    }
    
    
    scope[global] merged: {
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_driver": "postgres"
    }
    
    
    [nonprod] dvar expanded result:
    {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    }
    
    
    scope[nonprod] merged: {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user"
    }
    
    
    [prod] dvar expanded result:
    {
    }
    
    
    scope[prod] merged: {
      "host_alias": "prod"
    }
    
    
    ---------group vars----------
    
    nonprod: {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user"
    }
    
    
    prod: {
      "host_alias": "prod"
    }
    
    
    global: {
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_driver": "postgres"
    }
    
    
    groups members:[dev staging prod]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    [dev] dvar expanded result:
    {
      "db_host": "nonpord_database.test.host",
      "A_DEV_ENV_VAR": "a_global_env_var"
    }
    
    
    scope[dev] merged: {
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host",
      "A_DEV_ENV_VAR": "a_global_env_var"
    }
    
    
    merged[ dev ] runtime vars:
    {
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_host": "nonpord_database.test.host",
      "host_alias": "dev",
      "db_driver": "postgres",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_port": 8354,
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432
    }
    
    (core.Cache) (len=10) {
     (string) (len=7) "db_user": (string) (len=12) "test_db_user",
     (string) (len=11) "db_password": (string) (len=44) "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
     (string) (len=13) "A_DEV_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=4) "port": (int) 5432,
     (string) (len=23) "envVar_A_GLOBAL_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=7) "db_port": (int) 8354,
     (string) (len=10) "host_alias": (string) (len=3) "dev",
     (string) (len=9) "db_driver": (string) (len=8) "postgres",
     (string) (len=16) "A_GLOBAL_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=7) "db_host": (string) (len=26) "nonpord_database.test.host"
    }
    
    [runtime global] dvar expanded result:
    {
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "db_port": 8354,
      "port": 5432,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "host_alias": "dev",
      "db_driver": "postgres",
      "db_hostname": "dev.myapp.com",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "exec_vars"
          }
        },
        {
          "name": "assert",
          "cmd": {
            "{{eq .A_GLOBAL_ENV_VAR \"a_global_env_var\"}}",
            "{{eq .A_DEV_ENV_VAR \"a_global_env_var\"}}",
            "{{eq .db_host \"devtest_database.mycompany.local\"}}",
            "{{eq .db_url \"jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true\"}}"
          }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "A_DEV_ENV_VAR": "a_global_env_var",
      "host_alias": "dev",
      "db_driver": "postgres",
      "db_hostname": "dev.myapp.com",
      "db_port": 8354,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "port": 5432,
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "port": 5432,
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "host_alias": "dev",
      "db_port": 8354,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "db_hostname": "dev.myapp.com",
      "A_DEV_ENV_VAR": "a_global_env_var"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "port": 5432,
      "db_driver": "postgres",
      "db_hostname": "dev.myapp.com",
      "db_port": 8354,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "host_alias": "dev"
    })
    
    [exec_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "port": 5432,
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "host_alias": "dev",
      "db_driver": "postgres",
      "db_hostname": "dev.myapp.com",
      "db_port": 8354
    })
    
    [{{eq .A_GLOBAL_ENV_VAR "a_global_env_var"}} {{eq .A_DEV_ENV_VAR "a_global_env_var"}} {{eq .db_host "devtest_database.mycompany.local"}} {{eq .db_url "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"}}]
    ~SubStep2: [assert:  ]
     1 ASSERT OK:     [{{eq .A_GLOBAL_ENV_VAR "a_global_env_var"}}]
     2 ASSERT OK:     [{{eq .A_DEV_ENV_VAR "a_global_env_var"}}]
     3 ASSERT FAILED: [{{eq .db_host "devtest_database.mycompany.local"}}]
     4 ASSERT OK:     [{{eq .db_url "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"}}]
    
```

##### Logs with different verbose level
* [c0153 log - verbose level v](../../logs/c0153_v)
* [c0153 log - verbose level vv](../../logs/c0153_vv)
* [c0153 log - verbose level vvv](../../logs/c0153_vvv)
* [c0153 log - verbose level vvvv](../../logs/c0153_vvvv)
* [c0153 log - verbose level vvvvv](../../logs/c0153_vvvvv)

##### References
* [Related Chapter](../../user-interaction/c0153)
