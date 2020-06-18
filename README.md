# smith.js v 0.0.1

//smith is a library created by 
//anand and Andy.


function exchange(xarray,xvalue,xresult){
let nv="";
for(i=0;i<xarray[0].length;i++){
if(xarray[0][i]!=xvalue){
nv+=xarray[0][i]
}else{
nv+=xresult;
}
}
return nv;
}

// array 1st value access 
function array1st(smitharray, smitharrayvalue){
smitharray[0]=smitharrayvalue;
}

//choosing element
function choose(chooseid){
let nchooseid=chooseid.slice(1)
if(chooseid[0]=="#"){
return document.getElementById(nchooseid);
}else if(chooseid[0]=="."){
return document.getElementsByClassName(nchooseid);
}else{
return document.getElementsByTagName(nchooseid);
}
}

// if splice method 
function ifsplice(iarray, icondition, ival,ifirst,isecond){
if(icondition==">"){
if(iarray.length > ival){
me.splice(ifirst,isecond)
}
}

if(icondition=="<"){
if(iarray.length < ival){
me.splice(ifirst,isecond)
}
}

if(icondition==">="){
if(iarray.length >= ival){
me.splice(ifirst,isecond)
}
}
if(icondition=="<="){
if(iarray.length <= ival){
me.splice(ifirst,isecond)
}
}
if(icondition=="=="){
if(iarray.length == ival){
me.splice(ifirst,isecond)
}
}
if(icondition=="!="){
if(iarray.length != ival){
me.splice(ifirst,isecond)
}
}
}

//print
function p(smithtext){
console.log(smithtext);
}

//write
function write(smithtext){
document.write(smithtext)
}

//alert
function a(sval){
alert(sval)
}

//css for adding style
function css(sid,sstyle){
let nsid=sid.slice(1)

if(sid[0]=="#"){
document.getElementById(nsid).style=sstyle;
}else if(sid[0]=="."){
document.getElementsByClassName(nsid)[0].style=sstyle;
}else{
document.getElementsByTagName(sid)[0].style=sstyle;
}
}

var smath={
//power function
powerf:(spower)=>{
return x=>x**spower;},

//multiply

multi:(smulti)=>{
return x=>smulti*x;
},

//fact
fact:(sfact)=>{
if(sfact==1){
return 1;
}
return smath.fact(sfact-1)*sfact;
},

//add
add:(sone,stwo)=>{
return sone+stwo;
},

//sub
sub:(sone,stwo)=>{
return sone-stwo;
},

//square
square:(sval)=>{
return sval*sval;
},

//cube
cube:(sval)=>{
return sval*sval*sval;
},

//pow
pow:(sone,stwo)=>{
return sone**stwo;
},

//sqrt
sqrt:(sval)=>sval**(1/4)*sval**(1/4)
}

//isMatch
function isMatch(sstring,spattern){
let patt=new RegExp(spattern)
return patt.test(sstring);
}

//numSeperate
function numSeperate(sarray,doparse){
let tsarray=[]
for(let i of sarray){
if( !isNaN(i)){
if(doparse){
tsarray.push(parseInt(i))
}
else{
tsarray.push(i)
}

}}
return tsarray;
}

//strSeperate
function strSeperate(sarray){
let tsarray=[]
for(let i of sarray){
if( isNaN(i)){tsarray.push(i)}}
return tsarray;}

//strAdd
function strAdd(jj){
var jjv=jj.split(" ")
let sn=numSeperate(jjv,true)
let ss=strSeperate(jjv)
return smath.add(sn[0],sn[1]);
}
//Smith
