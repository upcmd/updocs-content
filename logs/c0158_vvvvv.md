---
title: "c0158_vvvvv"
date: 2020-10-07T00:11:29+1010:00
draft: false
weight: 11584

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0158
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
    loading [Task]:  ./tests/functests/c0158
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001779a0)((len=6 cap=6) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) (len=2) {
       (string) (len=9) "db_driver": (string) (len=8) "postgres",
       (string) (len=4) "port": (int) 5432
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
       (string) (len=7) "db_host": (string) (len=26) "nonpord_database.test.host",
       (string) (len=7) "db_port": (int) 8354,
       (string) (len=7) "db_user": (string) (len=12) "test_db_user",
       (string) (len=11) "db_password": (string) (len=34) "could_be_encrypted_using_upcmd_too"
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
       (string) (len=10) "host_alias": (string) (len=4) "prod",
       (string) (len=7) "db_host": (string) (len=25) "pord_database.proddb.host",
       (string) (len=7) "db_user": (string) (len=12) "prod_db_user"
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
      "port": 5432,
      "db_driver": "postgres",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var"
    }
    
    
    [nonprod] dvar expanded result:
    {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    }
    
    
    scope[nonprod] merged: {
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    }
    
    
    [prod] dvar expanded result:
    {
    }
    
    
    scope[prod] merged: {
      "host_alias": "prod"
    }
    
    
    ---------group vars----------
    
    nonprod: (*core.Cache)({
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user"
    })
    
    
    prod: (*core.Cache)({
      "host_alias": "prod"
    })
    
    
    global: (*core.Cache)({
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_driver": "postgres"
    })
    
    
    groups members:[dev staging prod]
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
    (*core.Cache)({
      "port": 5432,
      "db_driver": "postgres",
      "db_host": "nonpord_database.test.host",
      "host_alias": "dev",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_port": 8354,
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_user": "test_db_user",
      "A_DEV_ENV_VAR": "a_global_env_var"
    })
    
    (*core.Cache)(0xc0000b6a88)((len=10) {
     (string) (len=4) "port": (int) 5432,
     (string) (len=7) "db_port": (int) 8354,
     (string) (len=10) "host_alias": (string) (len=3) "dev",
     (string) (len=16) "A_GLOBAL_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=7) "db_host": (string) (len=26) "nonpord_database.test.host",
     (string) (len=9) "db_driver": (string) (len=8) "postgres",
     (string) (len=11) "db_password": (string) (len=44) "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
     (string) (len=13) "A_DEV_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=23) "envVar_A_GLOBAL_ENV_VAR": (string) (len=16) "a_global_env_var",
     (string) (len=7) "db_user": (string) (len=12) "test_db_user"
    })
    
    [runtime global] dvar expanded result:
    {
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "db_hostname": "dev.myapp.com",
      "port": 5432,
      "db_driver": "postgres",
      "db_port": 8354,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_host": "nonpord_database.test.host",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "host_alias": "dev",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    })
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "port": 5432,
      "db_user": "test_db_user",
      "host_alias": "dev",
      "db_driver": "postgres",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_port": 8354,
      "up_runtime_task_layer_number": 0,
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "up_runtime_task_layer_number": 0,
      "db_host": "nonpord_database.test.host",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "port": 5432,
      "db_port": 8354,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "host_alias": "dev",
      "db_driver": "postgres",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_user": "test_db_user"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_driver": "postgres",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "port": 5432,
      "db_port": 8354,
      "up_runtime_task_layer_number": 0,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host"
    })
    
    [exec_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_user": "test_db_user",
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host",
      "db_driver": "postgres",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "up_runtime_task_layer_number": 0,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "port": 5432,
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
* [c0158 log - verbose level v](../../logs/c0158_v)
* [c0158 log - verbose level vv](../../logs/c0158_vv)
* [c0158 log - verbose level vvv](../../logs/c0158_vvv)
* [c0158 log - verbose level vvvv](../../logs/c0158_vvvv)
* [c0158 log - verbose level vvvvv](../../logs/c0158_vvvvv)

##### References
* [Related Chapter](../../user-interaction/c0158)
