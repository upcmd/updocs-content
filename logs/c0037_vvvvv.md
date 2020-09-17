---
title: "c0037_vvvvv"
date: 2020-09-18T00:51:25+99:00
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
    (*impl.Scopes)(0xc00026ae40)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "ns": "prod",
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
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
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
      }
    }
    
    (core.Cache) (len=8) {
     (string) (len=2) "ns": (string) (len=4) "prod",
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
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=8) "teachers": ([]interface {}) (len=3 cap=3) {
       (string) (len=3) "tom",
       (string) (len=5) "jason",
       (string) (len=5) "alice"
      },
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "cbd": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom"
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
    "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k="
    
    -
    RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k=
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    -
    plaintext
    dvar> sprig_AES_key:
    "web_app-prod"
    
    -
    web_app-prod
    dvar> sprig_encrypt_AES_using_key_var:
    "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ="
    
    -
    ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=
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
    [runtime global] dvar expanded result:
    {
      "sprig_word_count": "3",
      "sprig_nospace": "helloworld",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_substring2": "0011",
      "sprig_date": "20200918",
      "sprig_upper": "WEB_APP",
      "sprig_encrypt_AES": "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k=",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "var_slice_index": "jason",
      "random_hello_plain": "hi, tom",
      "add1": "101",
      "convert_and_add1": "11",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "convert_and_add1_2": "11",
      "sprig_trim": "hello",
      "sprig_trim_prefix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_trim_suffix": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
      "random_hello": "Hello!",
      "sprig_muliply": "60",
      "sprig_AES_key": "web_app-prod",
      "sprig_encrypt_AES_using_key_var": "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=",
      "sprig_slice": "[jason alice]",
      "sprig_b64dec": "web_app ",
      "sprig_slice_contains": "true",
      "sprig_string_contains": "true",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim_all": "5.00",
      "sprig_substring": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_os_env": "/root"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_prefix": "hello",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_os_env": "/root",
      "sprig_slice_uniq": "[1 4 2 3 5]",
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
      "sprig_trim": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_substring2": "0011",
      "sprig_encrypt_AES_using_key_var": "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice_contains": "true",
      "pod_name": "web_app",
      "ha": true,
      "add1": "101",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_substring": "hello",
      "var_slice_index": "jason",
      "random_hello_plain": "hi, tom",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_string_contains": "true",
      "sprig_nospace": "helloworld",
      "age": 34,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice": "[jason alice]",
      "sprig_trim_all": "5.00",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_decrypt_AES": "plaintext",
      "ns": "prod",
      "old": 54,
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_date": "20200918",
      "convert_and_add1": "11",
      "sprig_muliply": "60",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_upper": "WEB_APP",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "add": "123",
      "sprig_word_count": "3",
      "sprig_encrypt_AES": "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k="
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
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES_using_key_var": "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "convert_and_add1": "11",
      "sprig_muliply": "60",
      "sprig_trim_prefix": "hello",
      "sprig_slice_contains": "true",
      "var_slice_index": "jason",
      "sprig_trim_suffix": "hello",
      "sprig_encrypt_AES": "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k=",
      "sprig_substring2": "0011",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "random_hello": "Hello!",
      "sprig_upper": "WEB_APP",
      "add": "123",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_filter_out": " [1 4] ",
      "convert_and_add1_2": "11",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_compact": "  [1 a foo]",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "up_runtime_task_layer_number": 0,
      "add1": "101",
      "sprig_string_contains": "true",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_word_count": "3",
      "pod_name": "web_app",
      "sprig_AES_key": "web_app-prod",
      "random_hello_plain": "hi, tom",
      "old": 54,
      "sprig_trim_all": "5.00",
      "sprig_substring": "hello",
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
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_b64dec": "web_app ",
      "ns": "prod",
      "sprig_decrypt_AES": "plaintext",
      "ha": true,
      "sprig_slice": "[jason alice]",
      "sprig_nospace": "helloworld",
      "age": 34,
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_date": "20200918",
      "sprig_os_env": "/root",
      "sprig_slice_uniq": "[1 4 2 3 5]"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "convert_and_add1": "11",
      "sprig_substring2": "0011",
      "sprig_os_env": "/root",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_all": "5.00",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_word_count": "3",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_muliply": "60",
      "sprig_slice": "[jason alice]",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "convert_and_add1_2": "11",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_upper": "WEB_APP",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_trim": "hello",
      "add1": "101",
      "age": 34,
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "add": "123",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "pod_name": "web_app",
      "sprig_string_contains": "true",
      "random_hello": "Hello!",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_encrypt_AES_using_key_var": "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=",
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
      "sprig_date": "20200918",
      "sprig_trim_suffix": "hello",
      "sprig_b64enc": "d2ViX2FwcA==",
      "var_slice_index": "jason",
      "sprig_b64dec": "web_app ",
      "ns": "prod",
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_AES_key": "web_app-prod",
      "up_runtime_task_layer_number": 0,
      "random_hello_plain": "hi, tom",
      "sprig_substring": "hello",
      "sprig_nospace": "helloworld",
      "sprig_trim_prefix": "hello",
      "sprig_slice_contains": "true",
      "sprig_encrypt_AES": "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k=",
      "old": 54,
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_decrypt_AES": "plaintext"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_encrypt_AES_using_key_var": "ekrF5E5Z7WKyQhlUGcgchU2WGysx1/JNliso9YzNEWQ=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "convert_and_add1": "11",
      "sprig_muliply": "60",
      "sprig_trim_prefix": "hello",
      "sprig_slice_contains": "true",
      "var_slice_index": "jason",
      "sprig_trim_suffix": "hello",
      "sprig_encrypt_AES": "RXpsZ2yFkQJ6wAHk5Ih7g9yRoji3LUylQ0WwxlNZq7k=",
      "sprig_substring2": "0011",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "random_hello": "Hello!",
      "sprig_upper": "WEB_APP",
      "add": "123",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_filter_out": " [1 4] ",
      "convert_and_add1_2": "11",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_trim": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_compact": "  [1 a foo]",
      "up_runtime_task_layer_number": 0,
      "add1": "101",
      "sprig_string_contains": "true",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_word_count": "3",
      "old": 54,
      "sprig_trim_all": "5.00",
      "pod_name": "web_app",
      "sprig_AES_key": "web_app-prod",
      "random_hello_plain": "hi, tom",
      "sprig_substring": "hello",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_b64dec": "web_app ",
      "ns": "prod",
      "sprig_decrypt_AES": "plaintext",
      "ha": true,
      "sprig_slice": "[jason alice]",
      "age": 34,
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_date": "20200918",
      "sprig_os_env": "/root",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_nospace": "helloworld",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "admins": {
        "tom",
        "jason",
        "alice"
      }
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
