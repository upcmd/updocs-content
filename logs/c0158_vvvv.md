---
title: "c0158_vvvv"
date: 2020-07-20T02:01:57+77:00
draft: false
weight: 11583

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0158
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
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_driver": "postgres",
      "port": 5432
    }
    
    
    groups members:[dev staging prod]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "db_user": "test_db_user",
      "db_host": "nonpord_database.test.host",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_port": 8354,
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "host_alias": "dev",
      "db_driver": "postgres",
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_port": 8354,
      "db_user": "test_db_user"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_hostname": "dev.myapp.com",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_hostname": "dev.myapp.com",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "host_alias": "dev",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars](*core.Cache)({
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user",
      "db_hostname": "dev.myapp.com",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "host_alias": "dev",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "port": 5432
    })
    
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
