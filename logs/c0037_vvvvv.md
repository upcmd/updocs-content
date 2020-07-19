---
title: "c0037_vvvvv"
date: 2020-07-20T02:01:35+77:00
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
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0037
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f8d40)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
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
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "age": 34,
      "old": 54
    }
    
    (core.Cache) (len=8) {
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
      (string) (len=7) "address": (map[string]interface {}) (len=2) {
       (string) (len=6) "suburb": (map[string]interface {}) (len=3) {
        (string) (len=4) "name": (string) (len=6) "sydney",
        (string) (len=8) "postcode": (int) 2000,
        (string) (len=3) "cbd": (bool) true
       },
       (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
      },
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=8) "teachers": ([]interface {}) (len=3 cap=3) {
       (string) (len=3) "tom",
       (string) (len=5) "jason",
       (string) (len=5) "alice"
      }
     },
     (string) (len=2) "ns": (string) (len=4) "prod",
     (string) (len=8) "pod_name": (string) (len=7) "web_app"
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
    "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34="
    
    dvar> sprig_decrypt_AES:
    "plaintext"
    
    dvar> sprig_AES_key:
    "web_app-prod"
    
    dvar> sprig_encrypt_AES_using_key_var:
    "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU="
    
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
    "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin "
    
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
      "add1": "101",
      "add": "123",
      "sprig_muliply": "60",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_slice_contains": "true",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_word_count": "3",
      "sprig_trim": "hello",
      "sprig_trim_all": "5.00",
      "sprig_nospace": "helloworld",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_os_env": "/root",
      "sprig_upper": "WEB_APP",
      "sprig_encrypt_AES_using_key_var": "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_substring2": "0011",
      "sprig_encrypt_AES": "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34=",
      "convert_and_add1_2": "11",
      "sprig_trim_suffix": "hello",
      "sprig_trim_prefix": "hello",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "random_hello_plain": "hi, tom",
      "sprig_decrypt_AES": "plaintext",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_slice": "[jason alice]",
      "var_slice_index": "jason",
      "convert_and_add1": "11"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "sprig_trim": "hello",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_encrypt_AES_using_key_var": "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU=",
      "age": 34,
      "convert_and_add1_2": "11",
      "random_hello_plain": "hi, tom",
      "sprig_decrypt_AES": "plaintext",
      "add": "123",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_muliply": "60",
      "sprig_slice_contains": "true",
      "sprig_word_count": "3",
      "admins": {
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
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_slice": "[jason alice]",
      "var_slice_index": "jason",
      "sprig_upper": "WEB_APP",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "sprig_nospace": "helloworld",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "sprig_slice_new": "[1 2 3 4 5]",
      "sprig_substring2": "0011",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_os_env": "/root",
      "ha": true,
      "sprig_trim_suffix": "hello",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_b64dec": "web_app ",
      "random_hello": "Hello!",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_trim_all": "5.00",
      "pod_name": "web_app",
      "old": 54,
      "sprig_encrypt_AES": "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34=",
      "sprig_trim_prefix": "hello",
      "convert_and_add1": "11",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_AES_key": "web_app-prod",
      "add1": "101"
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
      "sprig_repeat_with_space": " [web_app] ",
      "pod_name": "web_app",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_decrypt_AES": "plaintext",
      "sprig_muliply": "60",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_trim_suffix": "hello",
      "sprig_encrypt_AES": "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34=",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "convert_and_add1_2": "11",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_nospace": "helloworld",
      "sprig_os_env": "/root",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_upper": "WEB_APP",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "add": "123",
      "var_slice_index": "jason",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "sprig_substring2": "0011",
      "random_hello": "Hello!",
      "old": 54,
      "random_hello_plain": "hi, tom",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "ha": true,
      "sprig_trim_all": "5.00",
      "add1": "101",
      "sprig_encrypt_AES_using_key_var": "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU=",
      "sprig_trim": "hello",
      "sprig_slice": "[jason alice]",
      "sprig_slice_contains": "true",
      "sprig_b64dec": "web_app ",
      "sprig_trim_prefix": "hello",
      "convert_and_add1": "11",
      "age": 34,
      "sprig_word_count": "3",
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
      },
      "sprig_slice_append": "  [1 2 3 4 5 6] "
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "sprig_substring": "hello",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "add": "123",
      "var_slice_index": "jason",
      "age": 34,
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "convert_and_add1_2": "11",
      "add1": "101",
      "sprig_slice": "[jason alice]",
      "sprig_decrypt_AES": "plaintext",
      "random_hello_plain": "hi, tom",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_trim": "hello",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_upper": "WEB_APP",
      "sprig_os_env": "/root",
      "sprig_slice_contains": "true",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "old": 54,
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_encrypt_AES_using_key_var": "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU=",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_new": "[1 2 3 4 5]",
      "convert_and_add1": "11",
      "sprig_repeat_with_space": " [web_app] ",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_trim_suffix": "hello",
      "sprig_muliply": "60",
      "sprig_AES_key": "web_app-prod",
      "sprig_encrypt_AES": "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34=",
      "ns": "prod",
      "sprig_word_count": "3",
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
      "sprig_b64dec": "web_app ",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_substring2": "0011",
      "random_hello": "Hello!",
      "pod_name": "web_app",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "ha": true,
      "sprig_trim_prefix": "hello",
      "sprig_nospace": "helloworld",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_trim_all": "5.00"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "sprig_os_env": "/root",
      "sprig_dict_access_using_func": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]] ",
      "sprig_slice_reverse": "[5 4 3 2 1]",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "sprig_upper": "WEB_APP",
      "sprig_b64enc": "d2ViX2FwcA==",
      "sprig_slice_concat": "  [1 2 3 4 5 6 7 8] ",
      "sprig_os_env_expand": "Your path is set to /bin:/nix/var/nix/profiles/default/bin:/nix/var/nix/profiles/default/sbin:/bin:/sbin:/usr/bin:/usr/sbin ",
      "sprig_substring": "hello",
      "var_slice_index": "jason",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "sprig_substring2": "0011",
      "random_hello": "Hello!",
      "old": 54,
      "random_hello_plain": "hi, tom",
      "add": "123",
      "sprig_repeat": "web_appweb_appweb_app",
      "sprig_repeat_with_space_repeat": " [web_app]  [web_app]  [web_app] ",
      "sprig_slice_new": "[1 2 3 4 5]",
      "ha": true,
      "sprig_trim_all": "5.00",
      "add1": "101",
      "sprig_encrypt_AES_using_key_var": "fPlU/28E6ldrJp4FSF0j33RvXvNffjAYj7TtNGFO1xU=",
      "sprig_trim": "hello",
      "sprig_decrypt_AES_using_key_var": "plaintext",
      "sprig_slice_contains": "true",
      "sprig_b64dec": "web_app ",
      "sprig_trim_prefix": "hello",
      "convert_and_add1": "11",
      "age": 34,
      "sprig_word_count": "3",
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
      "sprig_slice": "[jason alice]",
      "sprig_slice_append": "  [1 2 3 4 5 6] ",
      "sprig_repeat_with_space": " [web_app] ",
      "pod_name": "web_app",
      "sprig_dict_access": " map[school:Sydney Grammar suburb:map[cbd:true name:sydney postcode:2000]]\n ",
      "sprig_decrypt_AES": "plaintext",
      "sprig_muliply": "60",
      "sprig_slice_compact": "  [1 a foo]",
      "sprig_dict": "  map[name1:value1 name2:value2 name3:value 3]\n value2 ",
      "sprig_slice_filter_out": " [1 4] ",
      "sprig_AES_key": "web_app-prod",
      "sprig_trim_suffix": "hello",
      "sprig_encrypt_AES": "P5yKbgUAw7fyvSJdiFQg8nL4VGS9Jwy5GF2u5+XUH34=",
      "sprig_slice_assign": " [1 2 3 4 5] ",
      "convert_and_add1_2": "11",
      "sprig_slice_uniq": "[1 4 2 3 5]",
      "sprig_nospace": "helloworld"
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
