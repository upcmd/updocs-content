---
title: "c0037_vvvv"
date: 2020-09-18T01:27:26+99:00
draft: false
weight: 10373

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0037
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
    loading [Task]:  ./tests/functests/c0037
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "student": {
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true
    }
    
    dvar> sprig_trim:
    "hello"
    
    -
    hello
    dvar> sprig_trim_all:
    "5.00"
    
    -
    5.00
    dvar> sprig_trim_suffix:
    "hello"
    
    -
    hello
    dvar> sprig_trim_prefix:
    "hello"
    
    -
    hello
    dvar> sprig_upper:
    "WEB_APP"
    
    -
    WEB_APP
    dvar> sprig_repeat:
    "web_appweb_appweb_app"
    
    -
    web_appweb_appweb_app
    dvar> sprig_repeat_with_space:
    " [web_app] "
    
    -
     [web_app] 
    dvar> sprig_repeat_with_space_repeat:
    " [web_app]  [web_app]  [web_app] "
    
    -
     [web_app]  [web_app]  [web_app] 
    dvar> sprig_substring:
    "hello"
    
    -
    hello
    dvar> sprig_nospace:
    "helloworld"
    
    -
    helloworld
    dvar> sprig_encrypt_AES:
    "GOUXklpwcF3x6KRSuS/bhkmmqaVMoqvHQE+ipgBLnCg="
    
    -
    GOUXklpwcF3x6KRSuS/bhkmmqaVMoqvHQE+ipgBLnCg=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "Z6BNpo3c9TynQAz0l7/xsPiyuotZIKrHQArUdSZvvMo="
    
    -
    Z6BNpo3c9TynQAz0l7/xsPiyuotZIKrHQArUdSZvvMo=
    dvar> sprig_decrypt_AES_using_key_var:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_slice:
    "[jason alice]"
    
    -
    [jason alice]
    dvar> sprig_slice_new:
    "[1 2 3 4 5]"
    
    -
    [1 2 3 4 5]
    dvar> sprig_slice_assign:
    " [1 2 3 4 5] "
    
    -
     [1 2 3 4 5] 
    dvar> sprig_slice_append:
    "  [1 2 3 4 5 6] "
    
    -
      [1 2 3 4 5 6] 
    dvar> sprig_slice_concat:
    "  [1 2 3 4 5 6 7 8] "
    
    -
      [1 2 3 4 5 6 7 8] 
    dvar> sprig_slice_reverse:
    "[5 4 3 2 1]"
    
    -
    [5 4 3 2 1]
    dvar> sprig_slice_uniq:
    "[1 4 2 3 5]"
    
    -
    [1 4 2 3 5]
    dvar> var_slice_index:
    "jason"
    
    -
    jason
    dvar> sprig_slice_filter_out:
    " [1 4] "
    
    -
     [1 4] 
    dvar> sprig_slice_contains:
    "true"
    
    -
    true
    dvar> sprig_string_contains:
    "true"
    
    -
    true
    dvar> sprig_slice_compact:
    "  [1 a foo]"
    
    -
      [1 a foo]
    dvar> sprig_b64enc:
    "d2ViX2FwcA=="
    
    -
    d2ViX2FwcA==
    dvar> sprig_b64dec:
    "web_app "
    
    -
    web_app 
    dvar> random_hello:
    "Hello!"
    
    -
    Hello!
    dvar> random_hello_plain:
    "hi, tom"
    
    -
    hi, tom
    dvar> sprig_os_env:
    "/root"
    
    -
    /root
    dvar> sprig_os_env_expand:
    "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin "
    
    -
    Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin 
    dvar> sprig_dict:
    "  map[name1:value1 name2:value2 name3:value 3]\n value2 "
    
    -
      map[name1:value1 name2:value2 name3:value 3]
     value2 
    dvar> sprig_dict_access:
    " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n "
    
    -
     map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]
     
    dvar> sprig_dict_access_using_func:
    " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] "
    
    -
     map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] 
    dvar> add1:
    "101"
    
    -
    101
    dvar> add:
    "123"
    
    -
    123
    dvar> convert_and_add1:
    "11"
    
    -
    11
    dvar> convert_and_add1_2:
    "11"
    
    -
    11
    dvar> sprig_substring2:
    "0011"
    
    -
    0011
    dvar> sprig_word_count:
    "3"
    
    -
    3
    dvar> sprig_muliply:
    "60"
    
    -
    60
    dvar> sprig_date:
    "20200918"
    
    -
    20200918
    -------runtime global final merged with dvars-------
    
    {
      "sprig_slice_compact": "  [1 a foo]",
      "var_slice_index": "jason",
      "sprig_trim_all": "5.00",
      "sprig_encrypt_AES": "GOUXklpwcF3x6KRSuS/bhkmmqaVMoqvHQE+ipgBLnCg=",
      "sprig_string_contains": "true",
      "old": 54,
      "convert_and_add1": "11",
      "convert_and_add1_2": "11",
      "sprig_b64dec": "web_app ",
      "sprig_trim_suffix": "hello",
      "sprig_slice": "[jason alice]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "ha": true,
      "sprig_word_count": "3",
      "sprig_muliply": "60",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_nospace": "helloworld",
      "random_hello": "Hello!",
      "age": 34,
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "student": {
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        },
        "name": "Tom"
      },
      "pod_name": "web_app",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_os_env": "/root",
      "sprig_repeat_with_space": " [web_app] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "random_hello_plain": "hi, tom",
      "sprig_substring": "hello",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_encrypt_AES_using_key_var": "Z6BNpo3c9TynQAz0l7/xsPiyuotZIKrHQArUdSZvvMo=",
      "sprig_slice_contains": "true",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_substring2": "0011",
      "sprig_date": "20200918",
      "sprig_decrypt_AES": "plaintext",
      "sprig_AES_key": "web_app-prod",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim": "hello",
      "sprig_trim_prefix": "hello",
      "sprig_upper": "WEB_APP",
      "add1": "101",
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
      "sprig_slice_new": "[1 2 3 4 5]"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "sprig_string_contains": "true",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "pod_name": "web_app",
      "sprig_trim_all": "5.00",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_substring": "hello",
      "sprig_encrypt_AES": "GOUXklpwcF3x6KRSuS/bhkmmqaVMoqvHQE+ipgBLnCg=",
      "sprig_os_env": "/root",
      "ha": true,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "random_hello_plain": "hi, tom",
      "sprig_b64dec": "web_app ",
      "sprig_upper": "WEB_APP",
      "sprig_slice_contains": "true",
      "sprig_AES_key": "web_app-prod",
      "add1": "101",
      "old": 54,
      "random_hello": "Hello!",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_trim": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        }
      },
      "ns": "prod",
      "sprig_encrypt_AES_using_key_var": "Z6BNpo3c9TynQAz0l7/xsPiyuotZIKrHQArUdSZvvMo=",
      "sprig_date": "20200918",
      "sprig_trim_prefix": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "add": "123",
      "sprig_slice_new": "[1 2 3 4 5]",
      "up_runtime_task_layer_number": 0,
      "sprig_slice_filter_out": " [1 4] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_decrypt_AES": "plaintext",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_muliply": "60",
      "age": 34,
      "sprig_nospace": "helloworld",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice": "[jason alice]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_word_count": "3",
      "sprig_substring2": "0011",
      "convert_and_add1": "11",
      "var_slice_index": "jason",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] "
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_repeat_with_space": " [web_app] ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice": "[jason alice]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_nospace": "helloworld",
      "sprig_word_count": "3",
      "sprig_substring2": "0011",
      "convert_and_add1": "11",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "var_slice_index": "jason",
      "sprig_string_contains": "true",
      "pod_name": "web_app",
      "sprig_trim_all": "5.00",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_os_env": "/root",
      "sprig_substring": "hello",
      "sprig_encrypt_AES": "GOUXklpwcF3x6KRSuS/bhkmmqaVMoqvHQE+ipgBLnCg=",
      "random_hello_plain": "hi, tom",
      "sprig_slice_contains": "true",
      "sprig_AES_key": "web_app-prod",
      "sprig_upper": "WEB_APP",
      "sprig_b64dec": "web_app ",
      "ha": true,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "random_hello": "Hello!",
      "add1": "101",
      "old": 54,
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_trim": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "student": {
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom",
        "gender": "Male"
      },
      "ns": "prod",
      "sprig_encrypt_AES_using_key_var": "Z6BNpo3c9TynQAz0l7/xsPiyuotZIKrHQArUdSZvvMo=",
      "sprig_date": "20200918",
      "sprig_trim_prefix": "hello",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "add": "123",
      "sprig_slice_new": "[1 2 3 4 5]",
      "up_runtime_task_layer_number": 0,
      "sprig_slice_filter_out": " [1 4] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_muliply": "60",
      "age": 34,
      "sprig_decrypt_AES": "plaintext"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"
    -
    check the value of other dvar using vvvv flag print out
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0037 log - verbose level v](../../logs/c0037_v)
* [c0037 log - verbose level vv](../../logs/c0037_vv)
* [c0037 log - verbose level vvv](../../logs/c0037_vvv)
* [c0037 log - verbose level vvvv](../../logs/c0037_vvvv)
* [c0037 log - verbose level vvvvv](../../logs/c0037_vvvvv)

##### References
* [Related Chapter](../../template/c0037)
