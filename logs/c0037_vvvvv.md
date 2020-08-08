---
title: "c0037_vvvvv"
date: 2020-08-09T01:36:04+88:00
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
    (*impl.Scopes)(0xc0002f61a0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
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
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    (core.Cache) (len=8) {
     (string) (len=8) "pod_name": (string) (len=7) "web_app",
     (string) (len=2) "ha": (bool) true,
     (string) (len=3) "age": (int) 34,
     (string) (len=3) "old": (int) 54,
     (string) (len=6) "admins": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     },
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
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "cbd": (bool) true,
        (string) (len=4) "name": (string) (len=6) "sydney"
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male"
     },
     (string) (len=2) "ns": (string) (len=4) "prod"
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
    "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos="
    
    -
    fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8="
    
    -
    04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=
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
    [runtime global] dvar expanded result:
    {
      "sprig_slice": "[jason alice]",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "convert_and_add1_2": "11",
      "sprig_substring2": "0011",
      "sprig_word_count": "3",
      "sprig_trim_all": "5.00",
      "sprig_trim_prefix": "hello",
      "sprig_encrypt_AES": "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=",
      "sprig_encrypt_AES_using_key_var": "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=",
      "sprig_muliply": "60",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "convert_and_add1": "11",
      "sprig_substring": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "random_hello": "Hello!",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_os_env": "/root",
      "sprig_trim_suffix": "hello",
      "sprig_upper": "WEB_APP",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_nospace": "helloworld",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "add": "123",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_contains": "true",
      "sprig_b64enc": "d2ViX2FwcA==",
      "random_hello_plain": "hi, tom",
      "sprig_date": "20200809",
      "sprig_trim": "hello",
      "sprig_AES_key": "web_app-prod",
      "var_slice_index": "jason",
      "add1": "101",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_b64dec": "web_app ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin "
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "sprig_os_env": "/root",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_b64dec": "web_app ",
      "ns": "prod",
      "random_hello": "Hello!",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_substring": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_date": "20200809",
      "sprig_slice": "[jason alice]",
      "ha": true,
      "old": 54,
      "convert_and_add1": "11",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_nospace": "helloworld",
      "sprig_trim_suffix": "hello",
      "sprig_upper": "WEB_APP",
      "pod_name": "web_app",
      "age": 34,
      "sprig_substring2": "0011",
      "sprig_trim_prefix": "hello",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "var_slice_index": "jason",
      "sprig_trim": "hello",
      "sprig_AES_key": "web_app-prod",
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
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
      "sprig_slice_contains": "true",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "random_hello_plain": "hi, tom",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "add1": "101",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_word_count": "3",
      "sprig_muliply": "60",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
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
      "sprig_encrypt_AES": "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=",
      "sprig_encrypt_AES_using_key_var": "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=",
      "convert_and_add1_2": "11",
      "sprig_trim_all": "5.00"
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
      "random_hello_plain": "hi, tom",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "random_hello": "Hello!",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "old": 54,
      "sprig_slice_new": "[1 2 3 4 5]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_substring2": "0011",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "student": {
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
        },
        "name": "Tom"
      },
      "sprig_encrypt_AES": "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=",
      "sprig_encrypt_AES_using_key_var": "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=",
      "sprig_slice_filter_out": " [1 4] ",
      "pod_name": "web_app",
      "sprig_trim_prefix": "hello",
      "sprig_trim": "hello",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "ns": "prod",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_substring": "hello",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "convert_and_add1": "11",
      "var_slice_index": "jason",
      "ha": true,
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_b64dec": "web_app ",
      "age": 34,
      "sprig_AES_key": "web_app-prod",
      "sprig_word_count": "3",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_upper": "WEB_APP",
      "add1": "101",
      "add": "123",
      "sprig_slice_contains": "true",
      "convert_and_add1_2": "11",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_os_env": "/root",
      "sprig_date": "20200809",
      "sprig_nospace": "helloworld",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_muliply": "60",
      "sprig_slice": "[jason alice]",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_all": "5.00"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "convert_and_add1_2": "11",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "random_hello": "Hello!",
      "sprig_substring": "hello",
      "sprig_b64dec": "web_app ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_AES_key": "web_app-prod",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_nospace": "helloworld",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_encrypt_AES": "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "ns": "prod",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_os_env": "/root",
      "sprig_trim_suffix": "hello",
      "sprig_decrypt_AES": "plaintext",
      "old": 54,
      "var_slice_index": "jason",
      "sprig_word_count": "3",
      "sprig_muliply": "60",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "age": 34,
      "sprig_upper": "WEB_APP",
      "sprig_trim": "hello",
      "student": {
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
        },
        "name": "Tom",
        "gender": "Male"
      },
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_encrypt_AES_using_key_var": "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=",
      "sprig_slice_filter_out": " [1 4] ",
      "pod_name": "web_app",
      "sprig_slice": "[jason alice]",
      "sprig_slice_contains": "true",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_trim_all": "5.00",
      "random_hello_plain": "hi, tom",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_trim_prefix": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "add1": "101",
      "sprig_date": "20200809",
      "add": "123",
      "sprig_substring2": "0011",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "ha": true,
      "convert_and_add1": "11"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "random_hello": "Hello!",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "old": 54,
      "sprig_slice_new": "[1 2 3 4 5]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "random_hello_plain": "hi, tom",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_substring2": "0011",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_encrypt_AES": "fY4Nw/u745S+AYVbGKqtTnZbMoN9OS6OKRjuzzPRoos=",
      "sprig_encrypt_AES_using_key_var": "04ulT6adySfIHF0f/zCGNM0TYu9vEb3rv6WOctM1cv8=",
      "sprig_slice_filter_out": " [1 4] ",
      "pod_name": "web_app",
      "sprig_trim_prefix": "hello",
      "sprig_trim": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "student": {
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
        },
        "name": "Tom",
        "gender": "Male"
      },
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_substring": "hello",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "ns": "prod",
      "ha": true,
      "convert_and_add1": "11",
      "var_slice_index": "jason",
      "age": 34,
      "sprig_AES_key": "web_app-prod",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_b64dec": "web_app ",
      "sprig_upper": "WEB_APP",
      "add1": "101",
      "sprig_word_count": "3",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "convert_and_add1_2": "11",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_os_env": "/root",
      "sprig_date": "20200809",
      "sprig_nospace": "helloworld",
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
      "sprig_slice_contains": "true",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_muliply": "60",
      "sprig_slice": "[jason alice]",
      "sprig_trim_all": "5.00"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"<=
    check the value of other dvar using vvvv flag print out
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
