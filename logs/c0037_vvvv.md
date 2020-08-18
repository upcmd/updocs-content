---
title: "c0037_vvvv"
date: 2020-08-18T15:15:53+88:00
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
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
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
    "D+PkZgRpU5iLC8BzZ8KRB49ApWKUnch+/za6fxkjG2g="
    
    -
    D+PkZgRpU5iLC8BzZ8KRB49ApWKUnch+/za6fxkjG2g=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "TWfKoghv5lhYvIHYuEJafNrulmCi4EPUmRd/mn6YNWU="
    
    -
    TWfKoghv5lhYvIHYuEJafNrulmCi4EPUmRd/mn6YNWU=
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
    "20200817"
    
    -
    20200817
    -------runtime global final merged with dvars-------
    
    {
      "sprig_trim_all": "5.00",
      "sprig_date": "20200817",
      "random_hello_plain": "hi, tom",
      "sprig_trim": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "age": 34,
      "sprig_word_count": "3",
      "sprig_slice_contains": "true",
      "var_slice_index": "jason",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "add1": "101",
      "random_hello": "Hello!",
      "convert_and_add1_2": "11",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "ha": true,
      "pod_name": "web_app",
      "sprig_decrypt_AES": "plaintext",
      "sprig_encrypt_AES": "D+PkZgRpU5iLC8BzZ8KRB49ApWKUnch+/za6fxkjG2g=",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim_suffix": "hello",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
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
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        }
      },
      "sprig_trim_prefix": "hello",
      "sprig_substring": "hello",
      "sprig_upper": "WEB_APP",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_muliply": "60",
      "sprig_nospace": "helloworld",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_b64dec": "web_app ",
      "sprig_os_env": "/root",
      "sprig_AES_key": "web_app-prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_substring2": "0011",
      "sprig_encrypt_AES_using_key_var": "TWfKoghv5lhYvIHYuEJafNrulmCi4EPUmRd/mn6YNWU=",
      "sprig_slice": "[jason alice]",
      "convert_and_add1": "11",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_repeat": "web_appweb_appweb_app"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "convert_and_add1": "11",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_trim_prefix": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_nospace": "helloworld",
      "sprig_b64dec": "web_app ",
      "sprig_substring2": "0011",
      "ns": "prod",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES": "D+PkZgRpU5iLC8BzZ8KRB49ApWKUnch+/za6fxkjG2g=",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "random_hello_plain": "hi, tom",
      "age": 34,
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_decrypt_AES": "plaintext",
      "add1": "101",
      "sprig_substring": "hello",
      "sprig_trim_all": "5.00",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_encrypt_AES_using_key_var": "TWfKoghv5lhYvIHYuEJafNrulmCi4EPUmRd/mn6YNWU=",
      "sprig_date": "20200817",
      "add": "123",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_upper": "WEB_APP",
      "sprig_slice_contains": "true",
      "pod_name": "web_app",
      "sprig_muliply": "60",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim": "hello",
      "sprig_word_count": "3",
      "var_slice_index": "jason",
      "convert_and_add1_2": "11",
      "old": 54,
      "sprig_trim_suffix": "hello",
      "sprig_os_env": "/root",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice": "[jason alice]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "random_hello": "Hello!",
      "ha": true
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_os_env": "/root",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice": "[jason alice]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "random_hello": "Hello!",
      "ha": true,
      "sprig_trim_suffix": "hello",
      "convert_and_add1": "11",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_trim_prefix": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_nospace": "helloworld",
      "sprig_b64dec": "web_app ",
      "sprig_substring2": "0011",
      "ns": "prod",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES": "D+PkZgRpU5iLC8BzZ8KRB49ApWKUnch+/za6fxkjG2g=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "random_hello_plain": "hi, tom",
      "age": 34,
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "add1": "101",
      "sprig_trim_all": "5.00",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "student": {
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "sprig_substring": "hello",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_encrypt_AES_using_key_var": "TWfKoghv5lhYvIHYuEJafNrulmCi4EPUmRd/mn6YNWU=",
      "sprig_date": "20200817",
      "add": "123",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_upper": "WEB_APP",
      "sprig_slice_contains": "true",
      "pod_name": "web_app",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim": "hello",
      "sprig_word_count": "3",
      "var_slice_index": "jason",
      "convert_and_add1_2": "11",
      "old": 54,
      "sprig_muliply": "60"
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
