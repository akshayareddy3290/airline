import java.util.scanner;
public class
Airline Reservation system {
boolean[] Arrseats =new
boolean[10];
scanner sc=new
scanner (system.in);
//SETTERS
//assings first empty seat in relevant section
public boolean
assign seat(string section){
if(section == "first"){
for(int i=0; i<5;i++){
if(arr seats[i])==false{
arrseats [i]= true;
print Boarding Pass(i);
return
true;
}
}
}
}else if (section == "economy"){
if(get free seats (section)>0){for(int i=5; i<arrseats.length;i++){
if (arrseats[i]==false){
arrseats[i]=true;
print boarding pass (i);
return
true;
}
}
}
}
//seats in chosen section full
//check if ok to assign to other section 
system.out.printf("all seats in section\"%s\"are booked,\n",section);
system.out.printf("would you like to be moved to section \"%s\" (y/n)?",
(section=="first") ?"economy":"first");
if(sc.next().charAt(0)== 'y')
assignseat((section=="first")?"economy":"first");
else
system.out.printf("\nNext flight leaves in 3 hours.\n");
return false;
}
//GETTERS
//returns number of free seats in each section 
private int
getFreeseats(strings section){
//first class 1-5
(array 0-4)
for(int i=0;i<5;i++){
if(arrseats[i]=="economy"){
//economy 6-10(array 5-9)
for(int i=5;
i<arrseats,length;i++){
if(arrseats[i]==false)
total +=1;
}
}
return total;
}
//see whether or not all seats are booked
public boolean
seatsAvailable(){
//if empty seat found 
return true 
for(boolean seat :arrseats)
if(seat==false)
return true;
//if none found plane is full
return false;
}
pubilc void printGreeting(){
system.out.println("\nWelcome to crap Airlines booking system.\n");
}
//print the menu with remaining number of seats for each section 
public void printmenu(){
system.out.printf("1.economy class %s\n",
(getfreeseats("first")>0?")"+
integer.tostring(getfreeseats("first"))+")": "(full)"));
system.out.print(">");
}
//print the boarding pass
private void 
printboardingpass(int seat){
system.out.println("\nboarding pass for crap Airlines .");
system.out.printf("\nSECTION:%s\nSEAT NUMBER:%d\n\n\n",(seat<5)?
"first":"economy",seat+1);
}
}
