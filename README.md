#Assignment No 5
## Introduction to Artificial Intelligence
## CSCI 6550

#Author
-NAME : SOHAN M.NIPUNAGE

-UGAID: 811 929 772

-EMAIL: smn57958@uga.edu

#Contents
1. FolDemo.java
2. FOLKnowledgeBaseFactory.java
3. DomainFactory.java
4. Output.txt

-----------------------------------------------------------------------------------------------

#Installation
Running AIMA code on Nike.

Set the classpath by typing the following command from the Nike prompt:

    > export CLASSPATH=''my path to''/aima-java/release/*:‘‘my path to’’/aima-java/aima-core/lib/*:.

Check your environment so see that the new classpath appears by typing:

    > env
    
• You will be using the `aima.core.logic.fol.*` package of AIMA. You may view
it at:

    “my path to”/aima-java/aima-core/src/main/java/aima/core/logic/fol


• If the classpath is set correctly, you can now use any of the functions defined
in the `aima.core.logic.fol.*` package.

• You are now ready to try out the code. Copy `FolDemo.java DomainFactory.java FOLKnowledgeBaseFactory.java` to your home directory


• Compile the java file by typing the following command:

    > javac FolDemo.java DomainFactory.java FOLKnowledgeBaseFactory.java
    
• Open `FolDemo.java` in your favorite editor to edit or modify. For example, if you are using vi,
then type the following command:

    > vi FolDemo.java
    
Run the compiled code by typing the following command:

    > java FolDemo
    
#Executing for Family Knowledge Base

##1 Family Tree :

*(THIS IS WITH REFERENCE TO ME, IE SOHAN)*

1. GRANDFATHER : MADHUKAR (GRANDFATHER OF SOHAN)

2. GRANDFATHER HAS THREE CHILDREN : 

  2.1 MILIND - FATHER OF SOHAN
  
  2.2 DILIP  - UNCLE OF SOHAN
  
  2.3 VARSHA - AUNT OF SOHAN
  
  2.4 MILIND IS BROTHER OF DILIP AND VARSHA
  
  2.5 DILIP IS BROTHER OF MILIND AND VARSHA
  
  2.6 VARSHA IS SISTER OF MILIND AND DILIP
  
  
3. SHUBHANGI - MOTHER OF SOHAN

4. MILIND AND SHUBHANGI ARE PARENTS OF SOHAN

5. MILIND AND SHUBHANGI HAVE TWO CHILDREN

  5.1 SOHAN IS THEIR SON
  
  5.2 PRIYANKA IS THEIR DAUGHTER

6. SOHAN IS BROTHER OF PRIYANKA

7. PRIYANKA IS SISTER OF SOHAN

##2 EXECUTION OF COMMANDS TO CHECK FOL

1. RUN FolDemo.java and it will give all the required outputs 

*Output.txt file contains output for all queries.

*Output for one of the queries :
`
Query :SISTER(x,SOHAN)
Proof, Answer Bindings: {x=PRIYANKA}
------------------------------------------------------------------------------------------------------------------------------------------------------------
|Step | Proof                                                                  |Justification                                                              |
------------------------------------------------------------------------------------------------------------------------------------------------------------
|1    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(MILIND,MILIND), {v36=MILIND, v35=MADHUKAR, v34=MILIND} |
|2    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(MILIND,VARSHA), {v36=VARSHA, v35=MADHUKAR, v34=MILIND} |
|3    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(MILIND,DILIP), {v36=DILIP, v35=MADHUKAR, v34=MILIND}   |
|4    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(SOHAN,SOHAN), {v36=SOHAN, v35=MILIND, v34=SOHAN}       |
|5    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(SOHAN,PRIYANKA), {v36=PRIYANKA, v35=MILIND, v34=SOHAN} |
|6    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(DILIP,VARSHA), {v36=VARSHA, v35=MADHUKAR, v34=DILIP}   |
|7    | MALE(v34) AND PARENT(v35,v34) AND PARENT(v35,v36) => BROTHER(v34,v36)  |Assert fact BROTHER(DILIP,DILIP), {v36=DILIP, v35=MADHUKAR, v34=DILIP}     |
|8    | FEMALE(v37) AND PARENT(v38,v37) AND PARENT(v38,v39) => SISTER(v37,v39) |Assert fact SISTER(PRIYANKA,SOHAN), {v39=SOHAN, v38=MILIND, v37=PRIYANKA}  |
------------------------------------------------------------------------------------------------------------------------------------------------------------
`
