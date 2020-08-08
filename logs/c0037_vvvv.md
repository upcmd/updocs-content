---
title: "c0037_vvvv"
date: 2020-08-09T01:36:04+88:00
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
      "pod_name": "web_app",
      "ha": true,
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
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          }
        }
      },
      "ns": "prod"
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
    "L0I/ECaSFwmoTqJdFN7aql8n5apw0M6i3w5ATjn2gWk="
    
    -
    L0I/ECaSFwmoTqJdFN7aql8n5apw0M6i3w5ATjn2gWk=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "eSC5zvcK3twH5PWC4Ve24mrNUxafE2S8B2SxZYQShFo="
    
    -
    eSC5zvcK3twH5PWC4Ve24mrNUxafE2S8B2SxZYQShFo=
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
    "20200809"
    
    -
    20200809
    -------runtime global final merged with dvars-------
    
    {
      "age": 34,
      "sprig_AES_key": "web_app-prod",
      "add": "123",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env": "/root",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "var_slice_index": "jason",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_upper": "WEB_APP",
      "sprig_substring2": "0011",
      "sprig_slice": "[jason alice]",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_substring": "hello",
      "random_hello_plain": "hi, tom",
      "sprig_repeat": "web_appweb_appweb_app",
      "ns": "prod",
      "sprig_trim_prefix": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "convert_and_add1": "11",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_date": "20200809",
      "ha": true,
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "add1": "101",
      "sprig_nospace": "helloworld",
      "sprig_slice_contains": "true",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "convert_and_add1_2": "11",
      "sprig_muliply": "60",
      "pod_name": "web_app",
      "old": 54,
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "sprig_encrypt_AES_using_key_var": "eSC5zvcK3twH5PWC4Ve24mrNUxafE2S8B2SxZYQShFo=",
      "sprig_encrypt_AES": "L0I/ECaSFwmoTqJdFN7aql8n5apw0M6i3w5ATjn2gWk=",
      "sprig_word_count": "3",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_suffix": "hello",
      "sprig_trim": "hello",
      "sprig_decrypt_AES": "plaintext",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_trim_all": "5.00"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
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
        }
      },
      "sprig_muliply": "60",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "random_hello_plain": "hi, tom",
      "ns": "prod",
      "pod_name": "web_app",
      "old": 54,
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_trim_all": "5.00",
      "add": "123",
      "age": 34,
      "sprig_slice": "[jason alice]",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_os_env": "/root",
      "sprig_upper": "WEB_APP",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_date": "20200809",
      "sprig_trim_prefix": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_nospace": "helloworld",
      "sprig_slice_new": "[1 2 3 4 5]",
      "convert_and_add1_2": "11",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_slice_filter_out": " [1 4] ",
      "var_slice_index": "jason",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_AES_key": "web_app-prod",
      "sprig_substring2": "0011",
      "convert_and_add1": "11",
      "ha": true,
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_encrypt_AES_using_key_var": "eSC5zvcK3twH5PWC4Ve24mrNUxafE2S8B2SxZYQShFo=",
      "sprig_encrypt_AES": "L0I/ECaSFwmoTqJdFN7aql8n5apw0M6i3w5ATjn2gWk=",
      "sprig_decrypt_AES": "plaintext",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "add1": "101",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_word_count": "3",
      "sprig_trim": "hello",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_contains": "true"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "sprig_muliply": "60",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "random_hello_plain": "hi, tom",
      "ns": "prod",
      "age": 34,
      "sprig_slice": "[jason alice]",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "pod_name": "web_app",
      "old": 54,
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_trim_all": "5.00",
      "add": "123",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_nospace": "helloworld",
      "sprig_os_env": "/root",
      "sprig_upper": "WEB_APP",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_date": "20200809",
      "sprig_trim_prefix": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "var_slice_index": "jason",
      "sprig_b64dec": "web_app ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "convert_and_add1_2": "11",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "random_hello": "Hello!",
      "sprig_AES_key": "web_app-prod",
      "sprig_substring2": "0011",
      "convert_and_add1": "11",
      "ha": true,
      "add1": "101",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_encrypt_AES_using_key_var": "eSC5zvcK3twH5PWC4Ve24mrNUxafE2S8B2SxZYQShFo=",
      "sprig_encrypt_AES": "L0I/ECaSFwmoTqJdFN7aql8n5apw0M6i3w5ATjn2gWk=",
      "sprig_decrypt_AES": "plaintext",
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
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_contains": "true",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_word_count": "3",
      "sprig_trim": "hello",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"<=
    check the value of other dvar using vvvv flag print out
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
