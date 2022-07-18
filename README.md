# database
https://www.simplilearn.com/tutorials/sql-tutorial/er-diagram-in-dbms
https://gitmind.com/er-diagram-tool.html#_10
https://erdplus.com/
https://erdplus.com/edit-diagram/60f12302-9a66-46dc-bcd9-926a858a70a0
https://www.tutorialspoint.com/explain-attributes-and-the-different-types-of-attributes-in-dbms


//***************************************************
var x=require("prompt-sync")();
var file=require("fs");
var z=require("./order");
var arr=[];
class Customer{
    constructor(){
        this.name;
        this.number;
        this.username;
        this.password;
    }
    newUser(input){
        if(input=="yes"){
          this.name=x("Enter the neame :");
          this.number=x("Enter the mobile number :");
          this.username=x("Enter the user name :");
          this.password=x("enter the password :")
        }
    }
    checking(input,name,pswd){
      if(input=="no"){
        var a="true";
        var result;
        console.log("checking")
        while(a!="false"){
        var fdata=file.readFileSync("customer.txt")
        var data=JSON.parse(fdata);
        arr.push(data);
        console.log(arr)

        arr.forEach((value)=>{
        if(value.password==name && value.name==pswd){
      if(n==this.name && i==this.id){
        console.log("******LOgin is success*****");
        result="login success";
        a="false";     
      }
      else{
        console.log("login failed pls try agin ")
        result="Login fail"
    }
  }
  return result;
});
}
}
}

searching(){
   var q1=x("Enter the ordered brand to search : ");
     if(q1=="redmi"){
       console.log("***Your order = "+z.order.ord+"***");
       return z.order.ord;   
   }
}
}
var a=new Customer();
var input=x("New user (yes/no)")
if(input=="yes"){
a.newUser(input);
var data=JSON.stringify(a,null,2);
file.writeFileSync("customer.txt",data);
}
else if(input=="no"){
var input1=x("Enter the usrname :");
var input2=x("Enter the pswd");
a.checking(input,input1,input2);
}
