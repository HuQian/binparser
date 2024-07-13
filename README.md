# binparser

```


FILE : (0,)
FILE.ELFHeader : (0,)
FILE.ELFHeader.Magic : (0,16)

on FILE.ELFHeader.Magic[0] == 0 {
    FILE.ELFHeader.Class : (17,17)
    FILE.ELFHeader.Data : (18,18)
}
on FILE.ELFHeader.Magic[0] == 1 {
    FILE.ELFHeader.Class : (17,17)
    FILE.ELFHeader.Data : (18,18)
}

FILE.ProgramHeaderTable : (${FILE.ELFHeader.poff}, +3)
loop n:FILE.ELFHeader.pnum {
    FILE.ProgramHeaderTable.PEntry${n} : (${n}, ${n}+10)
}



void p_hook (uint8* data, int size, char* path) {

}

{
    #header : 4b@3 : p_hook;
    #_ : 4b;
    #len : 4B;
    #data : {
        #m : 3B;
        #n : 4B;
        #g : ($data.m)B;
        #t : [{

        },{

        }]
    }
}

@define {
    8b : m;
    1b : n;
} Header


8b : h;
4b : m;
Header : d;


```

