---
title: "c0036_vvvvv"
date: 2020-08-18T15:15:53+88:00
draft: false
weight: 10364

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0036
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
    loading [Task]:  ./tests/functests/c0036
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00013fee0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
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
      },
      "managers": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    (core.Cache) (len=8) {
     (string) (len=10) "fieldnames": (map[string]interface {}) (len=1) {
      (string) (len=14) "name-with-dash": (string) (len=148) "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
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
     },
     (string) (len=8) "managers": ([]interface {}) (len=3 cap=3) {
      (string) (len=3) "tom",
      (string) (len=5) "jason",
      (string) (len=5) "alice"
     }
    }
    
    dvar> var_with_range:
    " x  x  x "
    
    -
     x  x  x 
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_test_log_auto_print:
    "prodweb_app"
    
    -
    prodweb_app
    dvar[object]> var_test_log_auto_print_object:
    "prodweb_app"
    
    dvar> var_with_and:
    "web_app"
    
    -
    web_app
    dvar> var_slice_index:
    "jason"
    
    -
    jason
    dvar> out_of_normal_field_name:
    "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
    
    -
    this_is_a_field_with_dash: you will have to use index func to access the field
    note: direct access this field will trigger template rendering error
    
    dvar> var_slice:
    "[jason]"
    
    -
    [jason]
    dvar> var_equal:
    "false"
    
    -
    false
    dvar> var_not_equal:
    "true"
    
    -
    true
    dvar> var_not_equal_another_way:
    "true"
    
    -
    true
    dvar> var_greater:
    "false"
    
    -
    false
    dvar> var_greater_and_equal:
    "true"
    
    -
    true
    dvar> var_greater_and_equal:
    "hello"
    
    -
    hello
    dvar> var_use_and_operator:
    "true"
    
    -
    true
    dvar> var_use_or_operator:
    "true"
    
    -
    true
    dvar> var_concat_values:
    "web_app: 34 years old"
    
    -
    web_app: 34 years old
    dvar> template_def:
    "\n\n\nONE TWO\"\n"
    
    -
    
    
    
    ONE TWO"
    
    [runtime global] dvar expanded result:
    {
      "var_commented_trimmed": "prod-web_app",
      "var_greater_and_equal": "hello",
      "var_length": "12",
      "var_slice_index": "jason",
      "var_use_and_operator": "true",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_greater": "false",
      "var_use_or_operator": "true",
      "var_space_trimmed": "prod-web_app",
      "var_commented": " prod-web_app",
      "var_not_equal": "true",
      "instance_full_name": "prod-web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_if": "prod-web_app-HA",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_not": "prod-web_app",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_with_not_object": "prod-web_app",
      "var_with_print": "prodweb_app",
      "var_test_log_auto_print": "prodweb_app",
      "var_slice": "[jason]",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_with_or": "prod",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_not_equal_another_way": "true",
      "var_concat_values": "web_app: 34 years old",
      "var_with_range": " x  x  x ",
      "var_with_ifelse": "prod-web_app-HA",
      "var_with_and": "web_app",
      "var_equal": "false"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "var_commented": " prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_not": "prod-web_app",
      "var_with_print": "prodweb_app",
      "age": 34,
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
      "var_equal": "false",
      "var_with_range": " x  x  x ",
      "var_test_log_auto_print": "prodweb_app",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_or": "prod",
      "var_slice": "[jason]",
      "var_with_and": "web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_with_if": "prod-web_app-HA",
      "var_not_equal": "true",
      "instance_full_name": "prod-web_app",
      "var_length": "12",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_with_range_item": " tom  jason  alice ",
      "var_slice_index": "jason",
      "var_use_and_operator": "true",
      "var_use_or_operator": "true",
      "var_commented_trimmed": "prod-web_app",
      "old": 54,
      "var_with_not_object": "prod-web_app",
      "var_not_equal_another_way": "true",
      "var_greater_and_equal": "hello",
      "var_greater": "false",
      "ha": true,
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_concat_values": "web_app: 34 years old",
      "ns": "prod",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "template_def": "\n\n\nONE TWO\"\n",
      "pod_name": "web_app",
      "var_with_ifelse": "prod-web_app-HA"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"{{.instance_full_name}}\"",
        "echo \"{{.var_space_not_trimmed}}\"",
        "echo \"{{.var_space_trimmed}}\"",
        "echo \"{{.var_commented}}\"",
        "echo \"{{.var_commented_trimmed}}\"",
        "echo \"{{.var_with_if}}\"",
        "echo \"{{.var_with_ifelse}}\"",
        "echo \"{{.var_with_ifelse_multilines}}\"",
        "echo \"{{.var_with_not}}\"",
        "echo \"{{.var_with_not_object}}\"",
        "echo \"{{.var_length}}\"",
        "echo \"{{.var_with_or}}\"",
        "echo \"{{.var_with_print}}\"",
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
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_space_trimmed": "prod-web_app",
      "var_not_equal_another_way": "true",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_commented_trimmed": "prod-web_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "ha": true,
      "var_equal": "false",
      "var_not_equal": "true",
      "var_use_and_operator": "true",
      "age": 34,
      "var_with_or": "prod",
      "var_with_if": "prod-web_app-HA",
      "var_use_or_operator": "true",
      "var_with_range_item": " tom  jason  alice ",
      "var_length": "12",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_greater": "false",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_print": "prodweb_app",
      "var_with_and": "web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "instance_full_name": "prod-web_app",
      "var_greater_and_equal": "hello",
      "pod_name": "web_app",
      "var_with_not": "prod-web_app",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_range": " x  x  x ",
      "var_slice_index": "jason",
      "var_with_not_object": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_commented": " prod-web_app",
      "var_test_log_auto_print": "prodweb_app",
      "var_slice": "[jason]",
      "var_concat_values": "web_app: 34 years old",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "ns": "prod",
      "var_with_ifelse": "prod-web_app-HA",
      "old": 54
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "age": 34,
      "var_with_or": "prod",
      "var_use_or_operator": "true",
      "var_with_print": "prodweb_app",
      "instance_full_name": "prod-web_app",
      "var_commented": " prod-web_app",
      "var_concat_values": "web_app: 34 years old",
      "var_with_ifelse": "prod-web_app-HA",
      "old": 54,
      "var_with_and": "web_app",
      "var_greater_and_equal": "hello",
      "var_slice": "[jason]",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_greater": "false",
      "var_with_not_object": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_test_log_auto_print": "prodweb_app",
      "var_use_and_operator": "true",
      "var_with_if": "prod-web_app-HA",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_not": "prod-web_app",
      "var_with_range": " x  x  x ",
      "var_space_trimmed": "prod-web_app",
      "var_with_range_item": " tom  jason  alice ",
      "pod_name": "web_app",
      "ns": "prod",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_slice_index": "jason",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "ha": true,
      "var_not_equal": "true",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_not_equal_another_way": "true",
      "var_length": "12",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_commented_trimmed": "prod-web_app",
      "var_equal": "false"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "var_greater_and_equal": "hello",
      "pod_name": "web_app",
      "var_with_not": "prod-web_app",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_range": " x  x  x ",
      "instance_full_name": "prod-web_app",
      "var_with_not_object": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_commented": " prod-web_app",
      "var_test_log_auto_print": "prodweb_app",
      "var_slice": "[jason]",
      "var_slice_index": "jason",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "ns": "prod",
      "var_with_ifelse": "prod-web_app-HA",
      "old": 54,
      "var_concat_values": "web_app: 34 years old",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_space_trimmed": "prod-web_app",
      "var_not_equal_another_way": "true",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_commented_trimmed": "prod-web_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "ha": true,
      "var_equal": "false",
      "var_not_equal": "true",
      "age": 34,
      "var_with_or": "prod",
      "var_with_if": "prod-web_app-HA",
      "var_use_or_operator": "true",
      "var_use_and_operator": "true",
      "var_length": "12",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_greater": "false",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_print": "prodweb_app",
      "var_with_and": "web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_with_range_item": " tom  jason  alice "
    })
    
    cmd( 1):
    echo "{{.instance_full_name}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.var_space_not_trimmed}}"
    
    cmd=>:
    echo "prod       -            web_app"
    -
    prod       -            web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=38) "echo \"prod       -            web_app\"",
     Code: (int) 0,
     Output: (string) (len=31) "prod       -            web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "{{.var_space_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "{{.var_commented}}"
    
    cmd=>:
    echo " prod-web_app"
    -
     prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=20) "echo \" prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "{{.var_commented_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "{{.var_with_if}}"
    
    cmd=>:
    echo "prod-web_app-HA"
    -
    prod-web_app-HA
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"prod-web_app-HA\"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo "{{.var_with_ifelse}}"
    
    cmd=>:
    echo "prod-web_app-HA"
    -
    prod-web_app-HA
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "echo \"prod-web_app-HA\"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 8):
    echo "{{.var_with_ifelse_multilines}}"
    
    cmd=>:
    echo "  prod-web_app-HA "
    -
      prod-web_app-HA 
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"  prod-web_app-HA \"",
     Code: (int) 0,
     Output: (string) (len=15) "prod-web_app-HA",
     ErrMsg: (string) ""
    }
    
    cmd( 9):
    echo "{{.var_with_not}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd(10):
    echo "{{.var_with_not_object}}"
    
    cmd=>:
    echo "prod-web_app"
    -
    prod-web_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"prod-web_app\"",
     Code: (int) 0,
     Output: (string) (len=12) "prod-web_app",
     ErrMsg: (string) ""
    }
    
    cmd(11):
    echo "{{.var_length}}"
    
    cmd=>:
    echo "12"
    -
    12
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=9) "echo \"12\"",
     Code: (int) 0,
     Output: (string) (len=2) "12",
     ErrMsg: (string) ""
    }
    
    cmd(12):
    echo "{{.var_with_or}}"
    
    cmd=>:
    echo "prod"
    -
    prod
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=11) "echo \"prod\"",
     Code: (int) 0,
     Output: (string) (len=4) "prod",
     ErrMsg: (string) ""
    }
    
    cmd(13):
    echo "{{.var_with_print}}"
    
    cmd=>:
    echo "prodweb_app"
    -
    prodweb_app
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"prodweb_app\"",
     Code: (int) 0,
     Output: (string) (len=11) "prodweb_app",
     ErrMsg: (string) ""
    }
    
    cmd(14):
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
* [c0036 log - verbose level v](../../logs/c0036_v)
* [c0036 log - verbose level vv](../../logs/c0036_vv)
* [c0036 log - verbose level vvv](../../logs/c0036_vvv)
* [c0036 log - verbose level vvvv](../../logs/c0036_vvvv)
* [c0036 log - verbose level vvvvv](../../logs/c0036_vvvvv)

##### References
* [Related Chapter](../../template/c0036)
