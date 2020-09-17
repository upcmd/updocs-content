---
title: "c0153_vvvv"
date: 2020-09-18T00:51:50+99:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0153
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    nonprod: {
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    }
    
    
    prod: {
      "host_alias": "prod"
    }
    
    
    global: {
      "port": 5432,
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_driver": "postgres"
    }
    
    
    groups members:[dev staging prod]
    merged[ dev ] runtime vars:
    {
      "port": 5432,
      "db_host": "nonpord_database.test.host",
      "db_user": "test_db_user",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_port": 8354,
      "host_alias": "dev",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_driver": "postgres",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY="
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "db_port": 8354,
      "host_alias": "dev",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "A_DEV_ENV_VAR": "a_global_env_var",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_host": "nonpord_database.test.host",
      "db_user": "test_db_user"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "up_runtime_task_layer_number": 0,
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "host_alias": "dev",
      "A_DEV_ENV_VAR": "a_global_env_var"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "A_DEV_ENV_VAR": "a_global_env_var",
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "host_alias": "dev",
      "db_driver": "postgres",
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "A_GLOBAL_ENV_VAR": "a_global_env_var",
      "db_user": "test_db_user",
      "db_password": "6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=",
      "envVar_A_GLOBAL_ENV_VAR": "a_global_env_var",
      "port": 5432,
      "db_hostname": "dev.myapp.com",
      "db_url": "jdbc:postgres://dev.myapp.com:8354/test?user=test_db_user&password=6HmsmiJIW1PfIXcF4WwOKOMDiL7PstgfKs2aRFajrwY=&ssl=true",
      "db_driver": "postgres",
      "up_runtime_task_layer_number": 0,
      "db_host": "nonpord_database.test.host",
      "db_port": 8354,
      "host_alias": "dev",
      "A_DEV_ENV_VAR": "a_global_env_var"
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
