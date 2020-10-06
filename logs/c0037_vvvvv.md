---
title: "c0037_vvvvv"
date: 2020-10-07T00:11:06+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    (*impl.Scopes)(0xc00027aea0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
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
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "ns": "prod",
      "pod_name": "web_app"
    })
    
    (*core.Cache)(0xc0000b6ae0)((len=8) {
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
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=8) "teachers": ([]interface {}) (len=3 cap=3) {
       (string) (len=3) "tom",
       (string) (len=5) "jason",
       (string) (len=5) "alice"
      },
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=3) "cbd": (bool) true,
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      }
     },
     (string) (len=2) "ns": (string) (len=4) "prod",
     (string) (len=8) "pod_name": (string) (len=7) "web_app",
     (string) (len=2) "ha": (bool) true,
     (string) (len=3) "age": (int) 34
    })
    
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
    "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI="
    
    -
    BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U="
    
    -
    rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=
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
    "20201006"
    
    -
    20201006
    [runtime global] dvar expanded result:
    {
      "sprig_trim_prefix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_AES_key": "web_app-prod",
      "var_slice_index": "jason",
      "sprig_slice_filter_out": " [1 4] ",
      "random_hello_plain": "hi, tom",
      "convert_and_add1_2": "11",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_nospace": "helloworld",
      "sprig_string_contains": "true",
      "sprig_decrypt_AES": "plaintext",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_b64dec": "web_app ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_word_count": "3",
      "sprig_trim": "hello",
      "sprig_trim_all": "5.00",
      "sprig_substring": "hello",
      "sprig_encrypt_AES_using_key_var": "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=",
      "sprig_slice_contains": "true",
      "add1": "101",
      "sprig_substring2": "0011",
      "sprig_encrypt_AES": "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "convert_and_add1": "11",
      "sprig_muliply": "60",
      "sprig_trim_suffix": "hello",
      "sprig_upper": "WEB_APP",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice_compact": "  [1 a foo]",
      "random_hello": "Hello!",
      "sprig_os_env": "/root",
      "add": "123",
      "sprig_date": "20201006",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice": "[jason alice]"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_trim": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "old": 54,
      "add": "123",
      "sprig_string_contains": "true",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_muliply": "60",
      "sprig_AES_key": "web_app-prod",
      "sprig_encrypt_AES_using_key_var": "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=",
      "random_hello": "Hello!",
      "sprig_upper": "WEB_APP",
      "sprig_word_count": "3",
      "pod_name": "web_app",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice": "[jason alice]",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "ha": true,
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_trim_suffix": "hello",
      "sprig_os_env": "/root",
      "convert_and_add1": "11",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_trim_all": "5.00",
      "sprig_b64dec": "web_app ",
      "sprig_trim_prefix": "hello",
      "age": 34,
      "add1": "101",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_substring": "hello",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "random_hello_plain": "hi, tom",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_encrypt_AES": "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=",
      "sprig_substring2": "0011",
      "ns": "prod",
      "sprig_date": "20201006",
      "var_slice_index": "jason",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
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
      "sprig_repeat_with_space": " [web_app] ",
      "convert_and_add1_2": "11",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_contains": "true",
      "sprig_nospace": "helloworld"
    })
    
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
      "sprig_encrypt_AES_using_key_var": "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=",
      "convert_and_add1": "11",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "add1": "101",
      "sprig_repeat_with_space": " [web_app] ",
      "convert_and_add1_2": "11",
      "pod_name": "web_app",
      "var_slice_index": "jason",
      "sprig_nospace": "helloworld",
      "ns": "prod",
      "sprig_encrypt_AES": "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=",
      "sprig_b64dec": "web_app ",
      "sprig_substring2": "0011",
      "ha": true,
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_contains": "true",
      "old": 54,
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_trim": "hello",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "random_hello": "Hello!",
      "up_runtime_task_layer_number": 0,
      "sprig_decrypt_AES": "plaintext",
      "sprig_string_contains": "true",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_trim_suffix": "hello",
      "sprig_substring": "hello",
      "sprig_os_env": "/root",
      "age": 34,
      "sprig_date": "20201006",
      "sprig_trim_all": "5.00",
      "add": "123",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice": "[jason alice]",
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
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "random_hello_plain": "hi, tom",
      "sprig_word_count": "3",
      "sprig_upper": "WEB_APP",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_muliply": "60",
      "sprig_trim_prefix": "hello",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_AES_key": "web_app-prod"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "up_runtime_task_layer_number": 0,
      "sprig_trim_prefix": "hello",
      "sprig_trim_suffix": "hello",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_contains": "true",
      "sprig_slice": "[jason alice]",
      "sprig_b64dec": "web_app ",
      "sprig_upper": "WEB_APP",
      "sprig_repeat_with_space": " [web_app] ",
      "old": 54,
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_word_count": "3",
      "sprig_decrypt_AES": "plaintext",
      "sprig_substring": "hello",
      "sprig_string_contains": "true",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "var_slice_index": "jason",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "add1": "101",
      "sprig_date": "20201006",
      "sprig_slice_new": "[1 2 3 4 5]",
      "random_hello": "Hello!",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
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
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "age": 34,
      "convert_and_add1_2": "11",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_substring2": "0011",
      "sprig_trim_all": "5.00",
      "pod_name": "web_app",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "convert_and_add1": "11",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim": "hello",
      "sprig_nospace": "helloworld",
      "sprig_muliply": "60",
      "add": "123",
      "sprig_encrypt_AES_using_key_var": "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=",
      "sprig_slice_filter_out": " [1 4] ",
      "random_hello_plain": "hi, tom",
      "sprig_encrypt_AES": "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_os_env": "/root",
      "sprig_slice_assign": " [1 2 3 4 5] "
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "old": 54,
      "sprig_b64dec": "web_app ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_encrypt_AES_using_key_var": "rN6qTdAMH5+kB5OzBbh/qR5P632QJmAjnQ9FJVrkz0U=",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_trim_suffix": "hello",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice": "[jason alice]",
      "sprig_decrypt_AES": "plaintext",
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
      "var_slice_index": "jason",
      "ns": "prod",
      "up_runtime_task_layer_number": 0,
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "ha": true,
      "sprig_muliply": "60",
      "sprig_upper": "WEB_APP",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_compact": "  [1 a foo]",
      "add1": "101",
      "sprig_date": "20201006",
      "convert_and_add1": "11",
      "sprig_trim_all": "5.00",
      "random_hello": "Hello!",
      "age": 34,
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_nospace": "helloworld",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "add": "123",
      "sprig_AES_key": "web_app-prod",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "convert_and_add1_2": "11",
      "sprig_string_contains": "true",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "random_hello_plain": "hi, tom",
      "sprig_word_count": "3",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_substring2": "0011",
      "sprig_os_env": "/root",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim": "hello",
      "sprig_slice_contains": "true",
      "sprig_encrypt_AES": "BTv5fDFrqUw33L35IX7o+fpllK8SLETZRsqQys6EQgI=",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_substring": "hello",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_prefix": "hello",
      "pod_name": "web_app",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext"
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
