---
title: "c0037_vvvv"
date: 2020-06-25T01:55:42+66:00
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
              ModuleName -> stupefied_noyce2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0037
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [stupefied_noyce2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
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
      "age": 34
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
    "X0iazz9vYb6p8sU8JBWO9pv1utW4pQeYyApyoYTePMA="
    
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    dvar> sprig_AES_key:
    "web_app-prod"
    
    dvar> sprig_encrypt_AES_using_key_var:
    "3o2cTKn2DFpty7WUMBNe6UHq3EE3rIXTlUSljyG4TGs="
    
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
    
    -------runtime global final merged with dvars-------
    
    {
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_decrypt_AES": "plaintext",
      "random_hello_plain": "hi, tom",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "add1": "101",
      "sprig_trim": "hello",
      "sprig_b64dec": "web_app ",
      "sprig_os_env": "/root",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_compact": "  [1 a foo]",
      "ha": true,
      "old": 54,
      "sprig_upper": "WEB_APP",
      "sprig_slice": "[jason alice]",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "convert_and_add1": "11",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "random_hello": "Hello!",
      "sprig_trim_prefix": "hello",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_word_count": "3",
      "sprig_trim_all": "5.00",
      "sprig_nospace": "helloworld",
      "sprig_substring2": "0011",
      "sprig_encrypt_AES": "X0iazz9vYb6p8sU8JBWO9pv1utW4pQeYyApyoYTePMA=",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "sprig_encrypt_AES_using_key_var": "3o2cTKn2DFpty7WUMBNe6UHq3EE3rIXTlUSljyG4TGs=",
      "var_slice_index": "jason",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "convert_and_add1_2": "11",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_substring": "hello",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_trim_suffix": "hello",
      "sprig_muliply": "60",
      "age": 34,
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
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_contains": "true",
      "sprig_AES_key": "web_app-prod",
      "ns": "prod",
      "pod_name": "web_app",
      "add": "123"
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
      "sprig_trim_all": "5.00",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "var_slice_index": "jason",
      "sprig_b64enc": "d2ViX2FwcA==",
      "age": 34,
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_trim_prefix": "hello",
      "convert_and_add1": "11",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_decrypt_AES": "plaintext",
      "random_hello_plain": "hi, tom",
      "sprig_trim_suffix": "hello",
      "sprig_AES_key": "web_app-prod",
      "sprig_trim": "hello",
      "ha": true,
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_contains": "true",
      "sprig_slice_filter_out": " [1 4] ",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
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
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_muliply": "60",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "pod_name": "web_app",
      "sprig_b64dec": "web_app ",
      "sprig_os_env": "/root",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice": "[jason alice]",
      "sprig_nospace": "helloworld",
      "sprig_encrypt_AES_using_key_var": "3o2cTKn2DFpty7WUMBNe6UHq3EE3rIXTlUSljyG4TGs=",
      "sprig_substring2": "0011",
      "add": "123",
      "old": 54,
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "random_hello": "Hello!",
      "convert_and_add1_2": "11",
      "sprig_substring": "hello",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "add1": "101",
      "sprig_upper": "WEB_APP",
      "sprig_encrypt_AES": "X0iazz9vYb6p8sU8JBWO9pv1utW4pQeYyApyoYTePMA=",
      "sprig_word_count": "3",
      "ns": "prod",
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
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin "
    })
    
    stupefied_noyce2: overall final exec vars:
    
    (*core.Cache)({
      "ha": true,
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_encrypt_AES": "X0iazz9vYb6p8sU8JBWO9pv1utW4pQeYyApyoYTePMA=",
      "sprig_b64enc": "d2ViX2FwcA==",
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
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "convert_and_add1_2": "11",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_substring": "hello",
      "convert_and_add1": "11",
      "sprig_trim_suffix": "hello",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "pod_name": "web_app",
      "random_hello": "Hello!",
      "sprig_substring2": "0011",
      "sprig_os_env_expand": "Your path is set to /bin:/root/.nix-profile/bin:/run/current-system/sw/bin ",
      "age": 34,
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "add": "123",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_trim": "hello",
      "sprig_b64dec": "web_app ",
      "add1": "101",
      "ns": "prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_trim_prefix": "hello",
      "var_slice_index": "jason",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice_contains": "true",
      "sprig_slice": "[jason alice]",
      "sprig_os_env": "/root",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_nospace": "helloworld",
      "sprig_encrypt_AES_using_key_var": "3o2cTKn2DFpty7WUMBNe6UHq3EE3rIXTlUSljyG4TGs=",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_word_count": "3",
      "sprig_trim_all": "5.00",
      "random_hello_plain": "hi, tom",
      "sprig_muliply": "60",
      "old": 54,
      "sprig_upper": "WEB_APP"
    })
    
    cmd( 1):
    echo "check the value of other dvar using vvvv flag print out"
    
     \_ echo "check the value of other dvar using vvvv flag print out"
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
