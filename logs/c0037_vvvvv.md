---
title: "c0037_vvvvv"
date: 2020-06-25T01:55:42+66:00
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
              ModuleName -> cranky_cori7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0037
    -------full vars in scopes------
    (*impl.Scopes)(0xc000290140)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cranky_cori7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "managers": {
        "tom",
        "jason",
        "alice"
      },
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
     (string) (len=2) "ns": (string) (len=4) "prod"
    }
    
    dvar> sprig_trim:
    "hello"
    
    dvar> sprig_trim_all:
    "5.00"
    
    dvar> sprig_trim_suffix:
    "hello"
    
    dvar> sprig_trim_prefix:
    "hello"
    
    dvar> sprig_upper:
    "WEB_APP"
    
    dvar> sprig_repeat:
    "web_appweb_appweb_app"
    
    dvar> sprig_repeat_with_space:
    " [web_app] "
    
    dvar> sprig_repeat_with_space_repeat:
    " [web_app]  [web_app]  [web_app] "
    
    dvar> sprig_substring:
    "hello"
    
    dvar> sprig_nospace:
    "helloworld"
    
    dvar> sprig_encrypt_AES:
    "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk="
    
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    dvar> sprig_AES_key:
    "web_app-prod"
    
    dvar> sprig_encrypt_AES_using_key_var:
    "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg="
    
    dvar> sprig_decrypt_AES_using_key_var:
    "plaintext"
    
    dvar> sprig_slice:
    "[jason alice]"
    
    dvar> sprig_slice_new:
    "[1 2 3 4 5]"
    
    dvar> sprig_slice_assign:
    " [1 2 3 4 5] "
    
    dvar> sprig_slice_append:
    "  [1 2 3 4 5 6] "
    
    dvar> sprig_slice_concat:
    "  [1 2 3 4 5 6 7 8] "
    
    dvar> sprig_slice_reverse:
    "[5 4 3 2 1]"
    
    dvar> sprig_slice_uniq:
    "[1 4 2 3 5]"
    
    dvar> var_slice_index:
    "jason"
    
    dvar> sprig_slice_filter_out:
    " [1 4] "
    
    dvar> sprig_slice_contains:
    "true"
    
    dvar> sprig_slice_compact:
    "  [1 a foo]"
    
    dvar> sprig_b64enc:
    "d2ViX2FwcA=="
    
    dvar> sprig_b64dec:
    "web_app "
    
    dvar> random_hello:
    "Hello!"
    
    dvar> random_hello_plain:
    "hi, tom"
    
    dvar> sprig_os_env:
    "/root"
    
    dvar> sprig_os_env_expand:
    "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin "
    
    dvar> sprig_dict:
    "  map[name1:value1 name2:value2 name3:value 3]\n value2 "
    
    dvar> sprig_dict_access:
    " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n "
    
    dvar> sprig_dict_access_using_func:
    " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] "
    
    dvar> add1:
    "101"
    
    dvar> add:
    "123"
    
    dvar> convert_and_add1:
    "11"
    
    dvar> convert_and_add1_2:
    "11"
    
    dvar> sprig_substring2:
    "0011"
    
    dvar> sprig_word_count:
    "3"
    
    dvar> sprig_muliply:
    "60"
    
    [runtime global] dvar expanded result:
    {
      "sprig_slice_contains": "true",
      "add1": "101",
      "sprig_substring2": "0011",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_encrypt_AES": "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk=",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_encrypt_AES_using_key_var": "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg=",
      "sprig_b64enc": "d2ViX2FwcA==",
      "add": "123",
      "sprig_trim": "hello",
      "sprig_substring": "hello",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_os_env": "/root",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_trim_prefix": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_word_count": "3",
      "sprig_slice_filter_out": " [1 4] ",
      "random_hello_plain": "hi, tom",
      "sprig_trim_all": "5.00",
      "sprig_trim_suffix": "hello",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "var_slice_index": "jason",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_upper": "WEB_APP",
      "sprig_nospace": "helloworld",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "convert_and_add1": "11",
      "convert_and_add1_2": "11",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice": "[jason alice]",
      "sprig_muliply": "60"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "sprig_decrypt_AES": "plaintext",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_nospace": "helloworld",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_os_env": "/root",
      "sprig_trim_all": "5.00",
      "sprig_trim_suffix": "hello",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ha": true,
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_encrypt_AES_using_key_var": "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg=",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "random_hello": "Hello!",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "sprig_word_count": "3",
      "sprig_slice_filter_out": " [1 4] ",
      "old": 54,
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "var_slice_index": "jason",
      "add1": "101",
      "sprig_substring2": "0011",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
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
      "age": 34,
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice": "[jason alice]",
      "sprig_trim": "hello",
      "sprig_trim_prefix": "hello",
      "pod_name": "web_app",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_substring": "hello",
      "random_hello_plain": "hi, tom",
      "sprig_b64dec": "web_app ",
      "sprig_upper": "WEB_APP",
      "convert_and_add1": "11",
      "convert_and_add1_2": "11",
      "sprig_muliply": "60",
      "sprig_encrypt_AES": "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk=",
      "sprig_slice_contains": "true",
      "add": "123",
      "ns": "prod",
      "admins": {
        "tom",
        "jason",
        "alice"
      }
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "age": 34,
      "pod_name": "web_app",
      "sprig_encrypt_AES_using_key_var": "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg=",
      "sprig_word_count": "3",
      "student": {
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
        },
        "name": "Tom"
      },
      "sprig_trim": "hello",
      "sprig_trim_prefix": "hello",
      "sprig_upper": "WEB_APP",
      "convert_and_add1": "11",
      "convert_and_add1_2": "11",
      "add": "123",
      "ha": true,
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice": "[jason alice]",
      "random_hello_plain": "hi, tom",
      "sprig_trim_suffix": "hello",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_compact": "  [1 a foo]",
      "random_hello": "Hello!",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_repeat": "web_appweb_appweb_app",
      "ns": "prod",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_decrypt_AES": "plaintext",
      "sprig_nospace": "helloworld",
      "sprig_trim_all": "5.00",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_substring": "hello",
      "sprig_muliply": "60",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "var_slice_index": "jason",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_substring2": "0011",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_contains": "true",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_os_env": "/root",
      "sprig_slice_filter_out": " [1 4] ",
      "add1": "101",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_b64dec": "web_app ",
      "sprig_encrypt_AES": "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk=",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin "
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_contains": "true",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_os_env": "/root",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "pod_name": "web_app",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_trim": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "random_hello": "Hello!",
      "sprig_slice": "[jason alice]",
      "sprig_nospace": "helloworld",
      "sprig_muliply": "60",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_repeat_with_space": " [web_app] ",
      "var_slice_index": "jason",
      "age": 34,
      "sprig_trim_prefix": "hello",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "random_hello_plain": "hi, tom",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_upper": "WEB_APP",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_word_count": "3",
      "convert_and_add1_2": "11",
      "add": "123",
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
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_substring": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "add1": "101",
      "sprig_encrypt_AES_using_key_var": "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg=",
      "convert_and_add1": "11",
      "sprig_trim_suffix": "hello",
      "sprig_substring2": "0011",
      "sprig_b64dec": "web_app ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_repeat": "web_appweb_appweb_app",
      "ns": "prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_encrypt_AES": "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk=",
      "ha": true,
      "sprig_trim_all": "5.00"
    }
    
    
    cranky_cori7: overall final exec vars:
    
    (*core.Cache)({
      "sprig_encrypt_AES": "oCiUnm01Zg9Xwf3o+Kn3ZtMk+o34Bo3EO4tb4q3vsYk=",
      "ha": true,
      "sprig_trim_all": "5.00",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_contains": "true",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_os_env": "/root",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "pod_name": "web_app",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_trim": "hello",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "random_hello": "Hello!",
      "sprig_slice": "[jason alice]",
      "sprig_nospace": "helloworld",
      "sprig_muliply": "60",
      "sprig_slice_compact": "  [1 a foo]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "age": 34,
      "sprig_trim_prefix": "hello",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "random_hello_plain": "hi, tom",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_upper": "WEB_APP",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_word_count": "3",
      "convert_and_add1_2": "11",
      "add": "123",
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
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_substring": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "add1": "101",
      "sprig_encrypt_AES_using_key_var": "A5qQ/f5Jg1Y32cm3s7Yk+227HQNdqueiYjvOkfpaDJg=",
      "convert_and_add1": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_b64dec": "web_app ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_repeat": "web_appweb_appweb_app",
      "ns": "prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "old": 54,
      "sprig_substring2": "0011"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
     \_ echo "check the value of other dvar using vvvv flag print out"
    check the value of other dvar using vvvv flag print out
     .. ok
    (utils.ExecResult) {
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
