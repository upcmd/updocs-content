---
title: "c0070_vvvv"
date: 2020-06-25T01:55:48+66:00
draft: false
weight: 10703

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0070
                 Verbose -> vvvv
              ModuleName -> loving_brattain7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0070
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [loving_brattain7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"\"\"school address {{.mystory}}\"\"\" > /tmp/mystory.txt",
        "cat /tmp/mystory.txt"
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
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    loving_brattain7: overall final exec vars:
    
    (*core.Cache)({
      "mystory": "  Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.\n\n    boa constrictor swallowing an animal\n  In the book it said: \"Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.\"\n\n  I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:\n\n    Drawing Number One\n    I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.\n\n  But they answered: \"Frighten? Why should any one be frightened by a hat?\"\n\n  My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w"
    })
    
    cmd( 1):
    echo """school address {{.mystory}}""" > /tmp/mystory.txt
    
     \_ echo """school address   Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.
    
        boa constrictor swallowing an animal
      In the book it said: "Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion."
    
      I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:
    
        Drawing Number One
        I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.
    
      But they answered: "Frighten? Why should any one be frightened by a hat?"
    
      My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w""" > /tmp/mystory.txt
    
     .. ok
    cmd( 2):
    cat /tmp/mystory.txt
    
     \_ cat /tmp/mystory.txt
    school address   Once when I was six years old I saw a magnificent picture in a book, called True Stories from Nature, about the primeval forest. It was a picture of a boa constrictor in the act of swallowing an animal. Here is a copy of the drawing.
    
        boa constrictor swallowing an animal
      In the book it said: Boa constrictors swallow their prey whole, without chewing it. After that they are not able to move, and they sleep through the six months that they need for digestion.
    
      I pondered deeply, then, over the adventures of the jungle. And after some work with a colored pencil I succeeded in making my first drawing. My Drawing Number One. It looked something like this:
    
        Drawing Number One
        I showed my masterpiece to the grown-ups, and asked them whether the drawing frightened them.
    
      But they answered: Frighten? Why should any one be frightened by a hat?
    
      My drawing was not a picture of a hat. It was a picture of a boa constrictor digesting an elephant. But since the grown-ups were not able to understand it, I made another drawing: I drew the inside of a boa constrictor, so that the grown-ups could see it clearly. They always need to have things explained. My Drawing Number Two looked like this:w
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0070 log - verbose level v](../../logs/c0070_v)
* [c0070 log - verbose level vv](../../logs/c0070_vv)
* [c0070 log - verbose level vvv](../../logs/c0070_vvv)
* [c0070 log - verbose level vvvv](../../logs/c0070_vvvv)
* [c0070 log - verbose level vvvvv](../../logs/c0070_vvvvv)

##### References
* [Related Chapter](../../dvars/c0070)