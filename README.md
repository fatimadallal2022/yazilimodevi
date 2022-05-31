# yazilimodevi
package com.plcoding.solidprinciplesandroid
import..
 
 class MainRepository(
 private val auth:FirebaseAuth)
 {
 suspend fun loginUser(email:string,password:string){
 try{
 auth.signInWithEmailAndPassword(email.password).await()
 }catch(e:Exception){
 val file =File(pathname:"errors.txt)
 file.appendText(
 text=e.message.toString()
 )
 }
 }
 }
