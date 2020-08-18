---
title: "c0037_vvvvv"
date: 2020-08-18T15:15:53+88:00
draft: false
weight: 10374

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0037
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f8d80)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
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
        },
        "name": "Tom"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "age": 34,
      "old": 54
    }
    
    (core.Cache) (len=8) {
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
     (string) (len=7) "student": (map[string]interface {}) (len=4) {
      (string) (len=8) "teachers": ([]interface {}) (len=3 cap=3) {
       (string) (len=3) "tom",
       (string) (len=5) "jason",
       (string) (len=5) "alice"
      },
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "cbd": (bool) true
       }
      },
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male"
     },
     (string) (len=2) "ns": (string) (len=4) "prod",
     (string) (len=8) "pod_name": (string) (len=7) "web_app",
     (string) (len=2) "ha": (bool) true,
     (string) (len=3) "age": (int) 34,
     (string) (len=3) "old": (int) 54,
     (string) (len=6) "admins": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     }
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
    "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig="
    
    -
    pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU="
    
    -
    ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=
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
    [runtime global] dvar expanded result:
    {
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_muliply": "60",
      "sprig_encrypt_AES": "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=",
      "sprig_upper": "WEB_APP",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_nospace": "helloworld",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "add1": "101",
      "add": "123",
      "convert_and_add1": "11",
      "sprig_trim_all": "5.00",
      "sprig_slice": "[jason alice]",
      "random_hello": "Hello!",
      "sprig_os_env": "/root",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_encrypt_AES_using_key_var": "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_date": "20200817",
      "sprig_AES_key": "web_app-prod",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_trim": "hello",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_slice_contains": "true",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_b64dec": "web_app ",
      "random_hello_plain": "hi, tom",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_substring2": "0011",
      "sprig_substring": "hello",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_word_count": "3",
      "sprig_decrypt_AES": "plaintext",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "var_slice_index": "jason",
      "sprig_slice_compact": "  [1 a foo]",
      "convert_and_add1_2": "11",
      "sprig_trim_prefix": "hello"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "sprig_nospace": "helloworld",
      "random_hello": "Hello!",
      "sprig_date": "20200817",
      "sprig_repeat": "web_appweb_appweb_app",
      "age": 34,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_trim_all": "5.00",
      "sprig_trim": "hello",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_AES_key": "web_app-prod",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "random_hello_plain": "hi, tom",
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
      "pod_name": "web_app",
      "add1": "101",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_trim_prefix": "hello",
      "sprig_encrypt_AES": "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=",
      "add": "123",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_word_count": "3",
      "sprig_upper": "WEB_APP",
      "sprig_b64dec": "web_app ",
      "sprig_slice": "[jason alice]",
      "sprig_os_env": "/root",
      "ha": true,
      "old": 54,
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_encrypt_AES_using_key_var": "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=",
      "sprig_substring": "hello",
      "sprig_slice_contains": "true",
      "ns": "prod",
      "var_slice_index": "jason",
      "convert_and_add1": "11",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "convert_and_add1_2": "11",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring2": "0011",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_trim_suffix": "hello",
      "sprig_b64enc": "d2ViX2FwcA==",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_muliply": "60",
      "sprig_slice_reverse": "[5 4 3 2 1]"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"check the value of other dvar using vvvv flag print out\""
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "age": 34,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_word_count": "3",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_new": "[1 2 3 4 5]",
      "random_hello": "Hello!",
      "sprig_date": "20200817",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice": "[jason alice]",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_encrypt_AES_using_key_var": "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=",
      "sprig_b64enc": "d2ViX2FwcA==",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_AES_key": "web_app-prod",
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
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_nospace": "helloworld",
      "add": "123",
      "sprig_upper": "WEB_APP",
      "ns": "prod",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_substring": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "add1": "101",
      "sprig_slice_compact": "  [1 a foo]",
      "old": 54,
      "sprig_slice_contains": "true",
      "var_slice_index": "jason",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_muliply": "60",
      "sprig_trim_all": "5.00",
      "sprig_trim_prefix": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_b64dec": "web_app ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "random_hello_plain": "hi, tom",
      "sprig_substring2": "0011",
      "sprig_trim": "hello",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES": "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=",
      "sprig_decrypt_AES": "plaintext",
      "sprig_os_env": "/root",
      "ha": true,
      "convert_and_add1": "11",
      "pod_name": "web_app"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sprig_encrypt_AES": "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=",
      "sprig_os_env": "/root",
      "sprig_AES_key": "web_app-prod",
      "sprig_upper": "WEB_APP",
      "var_slice_index": "jason",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_muliply": "60",
      "random_hello_plain": "hi, tom",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_b64dec": "web_app ",
      "sprig_trim": "hello",
      "age": 34,
      "sprig_word_count": "3",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "ns": "prod",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice": "[jason alice]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_trim_all": "5.00",
      "pod_name": "web_app",
      "convert_and_add1_2": "11",
      "sprig_encrypt_AES_using_key_var": "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_nospace": "helloworld",
      "sprig_trim_prefix": "hello",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_substring2": "0011",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_contains": "true",
      "ha": true,
      "random_hello": "Hello!",
      "sprig_date": "20200817",
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
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          }
        },
        "name": "Tom"
      },
      "sprig_substring": "hello",
      "add1": "101",
      "old": 54,
      "convert_and_add1": "11",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_repeat_with_space": " [web_app] ",
      "add": "123",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_trim_suffix": "hello"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_word_count": "3",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_new": "[1 2 3 4 5]",
      "age": 34,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice": "[jason alice]",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_encrypt_AES_using_key_var": "ObJzmuHB1hqA2Im/mJwVslNp9HUTyXUO0IksXdXrrKU=",
      "sprig_b64enc": "d2ViX2FwcA==",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "random_hello": "Hello!",
      "sprig_date": "20200817",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_AES_key": "web_app-prod",
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
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          }
        },
        "name": "Tom"
      },
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "add": "123",
      "sprig_upper": "WEB_APP",
      "ns": "prod",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_nospace": "helloworld",
      "sprig_substring": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "add1": "101",
      "sprig_slice_compact": "  [1 a foo]",
      "old": 54,
      "sprig_slice_contains": "true",
      "var_slice_index": "jason",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_muliply": "60",
      "sprig_trim_all": "5.00",
      "sprig_trim_prefix": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_b64dec": "web_app ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "random_hello_plain": "hi, tom",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES": "pPrh6In0KxQxF2x8/vlA1MvYMnRdK97Qq2sEIKhhRig=",
      "sprig_decrypt_AES": "plaintext",
      "sprig_os_env": "/root",
      "ha": true,
      "convert_and_add1": "11",
      "sprig_substring2": "0011",
      "sprig_trim": "hello",
      "pod_name": "web_app"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"
    -
    check the value of other dvar using vvvv flag print out
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=62) "echo \"check the value of other dvar using vvvv flag print out\"",
     Code: (int) 0,
     Output: (string) (len=55) "check the value of other dvar using vvvv flag print out",
     ErrMsg: (string) ""
    }
    
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
