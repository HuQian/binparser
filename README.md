# binparser

void p_hook (uint8* data, int size) {

}

{
    #header : [4b, 1] : p_hook;
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

