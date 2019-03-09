public class vaki {

private vaki north; //شمال _1
private vaki northeast;   //شمال شرق_2
private vaki east;   //شرق_3
private vaki southeast;  //جنوب شرق_4
private vaki south; //جنوب_5
private vaki southwest; //جنوب غرب_6
private vaki west; //غرب_7
private vaki northwest; //شمال غرب_8
private static int number_of_vaki=0; // for number of divice of vaki , for each divice increase on
private String text; // contain text
private static int number_of_ways=0; // number of ways that is find
private String message; // on method get_message it contain message of text
private static int only_print_ways=0; // just a switch on compair to not show doubles and long not foun ways
private String objectname; // name of object , in this version it should be number_of_vaki ,and not use constructure number 3 in this version
///////////////////////////////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////////////////////
public vaki(){
    number_of_vaki++;
    objectname=String.format("_"+number_of_vaki+"");///////////////////////////////
    north=null; //شمال
    northeast=null;   //شمال شرق
    east=null;   //شرق
    southeast=null;  //جنوب شرق
    south=null; //جنوب
    southwest=null; //جنوب غرب
    west=null; //غرب
    northwest=null;
} // constrocture for default  ____1
///////////////////////////////////////////////////////////////////////////////////////
public vaki(vaki _1 , vaki _2 , vaki _3 , vaki _4 , vaki _5 , vaki _6 , vaki _7 ,vaki _8  ){
    number_of_vaki++;
    objectname =String.format("_"+number_of_vaki);
    north=_1 ; //شمال
    northeast=_2;   //شمال شرق
    east=_3;   //شرق
    southeast=_4;  //جنوب شرق
    south=_5; //جنوب
    southwest=_6; //جنوب غرب
    west=_7; //غرب
    northwest=_8;//شمال غرب
} // constracture for manual ___2
///////////////////////////////////////////////////////////////////////////////////////
public vaki(String _objectname,vaki _1 , vaki _2 , vaki _3 , vaki _4 , vaki _5 , vaki _6 , vaki _7 ,vaki _8  ){
    number_of_vaki++;
    objectname = String.format("_"+_objectname);
    north=_1 ; //شمال
    northeast=_2;   //شمال شرق
    east=_3;   //شرق
    southeast=_4;  //جنوب شرق
    south=_5; //جنوب
    southwest=_6; //جنوب غرب
    west=_7; //غرب
    northwest=_8;//شمال غرب
} // constracture for manual ___3
///////////////////////////////////////////////////////////////////////////////////////
public void set_vaki(vaki _1 , vaki _2 , vaki _3 , vaki _4 , vaki _5 , vaki _6 , vaki _7 ,vaki _8 ){
    north=_1 ; //شمال
    northeast=_2;   //شمال شرق
    east=_3;   //شرق
    southeast=_4;  //جنوب شرق
    south=_5; //جنوب
    southwest=_6; //جنوب غرب
    west=_7; //غرب
    northwest=_8;//شمال غرب
} // set pointers fo object of vaki that is creat befor
///////////////////////////////////////////////////////////////////////////////////////
public void send (String _text){
    if(north==null){
    } else {
        north.recive(_text);
    }
    if(northeast==null){
    } else {
        northeast.recive(_text);
    }
    if(east==null){
    } else {
        east.recive(_text);
    }
    if(southeast==null){
    } else {
        southeast.recive(_text);
    }
    if(south==null){
    } else {
        south.recive(_text);
    }
    if(southwest==null){
    } else {
        southwest.recive(_text);
    }
    if(west==null){
    } else {
        west.recive(_text);
    }
    if(northwest==null){
    } else {
        northwest.recive(_text);
    }
} // send text to Devices that is not null
///////////////////////////////////////////////////////////////////////////////////////
public void recive(String _text){
    compair(_text);
} // reciver and send it to compair and compair chose to send it or not
///////////////////////////////////////////////////////////////////////////////////////
public void  compair(String _text){
        if (objectname.equals(get_Distination_from_text(_text))){
        text = String.format(_text+toString());
        number_of_ways++;
        System.out.format("found Destination on way:"+text+"\n");
        } // if this object is Destination jub is done
        else if (_text.contains(objectname)){
            if(only_print_ways!=1){ // for method get_only_print_ways to show 0 and not show 1 double ways or long not found ways
        System.out.format("double on way : "+_text+objectname+"\n");
            }
        } // if double node in way done it
        else if(_text.length()>=1000){
        text = String.format(_text+toString());
         if(only_print_ways!=1){ // for method get_only_print_ways to show 0 and not show 1 double ways or long not found ways
        System.out.format("Destination not found  in way:"+_text+"\n");
         }
        } // if way is get so far  => it note alow hedek
        else{
          text = String.format(_text+toString());
          send(text);
        } // if Destination is note this device and no problem sed it agen

} // compire dist whit it object name
///////////////////////////////////////////////////////////////////////////////////////
public String send_to_Destination(String Message ,vaki Destination){
    String _text;
    _text =String.format(Destination.toString()+"*"+ Message +"*"+toString());
    this.text= _text;
    return _text;
    // text contain Destination objectnumber +*massage*+sender objectnumber
} // just for sender divice ... add dest message and source to first fo text
///////////////////////////////////////////////////////////////////////////////////////
@Override
public String toString() {
         return String.format("_"+objectname +"_");
      }  // just for toString name of object
///////////////////////////////////////////////////////////////////////////////////////
public String get_number(){
return String.format("%d",number_of_vaki );
}
///////////////////////////////////////////////////////////////////////////////////////
private String get_Distination_from_text(String _text){
        // message is byand of * and befor massage is Destination
    return _text.substring(1,_text.indexOf("*")-1); // take the sertain part of String text that is byand of 1 and index-1

    } /// take Destination form text
public void get_Dest(){
    // call metod to put Destination from text to Destination
    System.out.println(get_Distination_from_text(text));
}      /// only print Destination
///////////////////////////////////////////////////////////////////////////////////////
private void get_message(){
    message=String.format(text.substring(text.indexOf("*"), text.lastIndexOf("*")));
} /// take message form text
public void get_mess(){
    get_message(); // run method to put message from text to message
    System.out.format(message); // show message
} // only show message
//////////////////////////////////////////////////////////////////////////////////////
public static void get_number_of_ways(){
    System.out.println(number_of_ways);
} //just returnd number of ways
/////////////////////////////////////////////////////////////////////////////////////
public static void only_print_ways(){
    only_print_ways=1;
}

}
