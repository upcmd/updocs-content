---
title: "c0153_vvvv"
date: 2020-07-20T02:01:56+77:00
draft: false
weight: 11533

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0153
    ---------group vars----------
    
    nonprod: {
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354
    }
    
    
    prod: {
      "host_alias": "prod"
    }
    
    
    global: {
      "db_driver": "postgres",
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var"
    }
    
    
    groups members:[dev staging prod]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "db_driver": "postgres",
      "port": 5432,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "A_DEV_ENV_VAR": "a_global_env_var",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "host_alias": "dev"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "host_alias": "dev",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_port": 8354,
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_hostname": "dev.myapp.com",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_host": "nonpord_database.test.host",
      "db_driver": "postgres"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "db_port": 8354,
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_user": "test_db_user",
      "db_host": "nonpord_database.test.host",
      "host_alias": "dev",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_driver": "postgres"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_host": "nonpord_database.test.host",
      "host_alias": "dev",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_port": 8354,
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres"
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "db_port": 8354,
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_user": "test_db_user",
      "db_host": "nonpord_database.test.host",
      "host_alias": "dev",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_driver": "postgres"
    })
    
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
