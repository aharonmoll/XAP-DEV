# xap-dev-training - lab9-exercise

## 9 Spring Introduction

###### Lab Goals
Experience Spring Framework in order to understand Open Spaces framework and API.
###### Lab Description
This exercise will demonstrate the same application developed 3 times each using a different method:
1.	A traditional Java application
2.	A Spring XML based application
3.	A Spring Annotations based application
You will explore the first 2 applications and code the 3rd application.
###### Lab setup
Make sure you restart gs-agent and gs-ui (or at least undeploy all Processing Units using gs-ui)

9.1.1 Create dir: %XAP_TRAINING_HOME%/labs/lab9-exercise

    mkdir /Users/yuval/XAPDevTraining/labs/lab9-exercise

9.1.2 Navigate to lab9-exercise dir

    cd /Users/yuval/XAPDevTraining/labs/lab9-exercise

9.1.3 Clone the git project

    git clone https://github.com/GigaSpaces-ProfessionalServices/xap-dev-training.git

9.1.4 Checkout lab9-exercise

    cd xap-dev-training
    git checkout lab9-exercise
    
9.1.5 Verify that the branch has been checked out.

    yuval-pc:xap-dev-training yuval$ git branch
    * lab9-exercise
      master
               
9.1.6 Open xap-dev-training project with intellij <br />
9.1.7 Run mvn install

    yuval-pc:xap-dev-training yuval$ mvn install
    
       [INFO] ------------------------------------------------------------------------
       [INFO] Reactor Summary:
       [INFO] 
       [INFO] Lab9-exercise 1.0-SNAPSHOT ......................... SUCCESS [  1.624 s]
       [INFO] BillBuddy_Space .................................... SUCCESS [  8.323 s]
       [INFO] BillBuddy_Space .................................... SUCCESS [  0.680 s]
       [INFO] Traditional_Java 1.0-SNAPSHOT ...................... SUCCESS [  2.176 s]
       [INFO] ------------------------------------------------------------------------
       [INFO] BUILD SUCCESS




9.1.8 Run mvn xap:intellij.
###### This will add the predefined Run Configuration Application to your Intellij IDE.

    yuval-pc:xap-dev-training yuval$ mvn xap:intellij
    
      [INFO] Reactor Summary:
      [INFO] 
      [INFO] Lab9-exercise 1.0-SNAPSHOT ......................... SUCCESS [  1.779 s]
      [INFO] BillBuddy_Space .................................... SKIPPED
      [INFO] BillBuddy_Space .................................... SKIPPED
      [INFO] Traditional_Java 1.0-SNAPSHOT ...................... SKIPPED
      [INFO] ------------------------------------------------------------------------
      [INFO] BUILD SUCCESS

Make sure you have a C:\temp directory on your computer. <br />
In case you do not have it will create the file inside Temp folder in your Traditional_Java folder. <br />
Notice the 3 projects; each is named according to the method type. <br />
Use the slides in order to recap the application design.  

## 9.2	Standard Java application
a.	Examine the classes and code of the application. <br />
    Especially examine the relationship between the classes. <br />
b.	Run the class com.c123.nospring.example.TraditionalMain in the Traditional_Java folder. <br />
c.	Check the output file (location is printed in the Intellij console) <br /> 
## 9.3	Spring XML based application
a.	Examine the classes and code of the application in the Spring_Xml folder. <br />
Validate you understand the wiring code and bean lifecycle processing by Spring. <br />
    Especially examine: <br />
a.	springContext.xml <br /> 
b.	com.c123.spring.example.SpringMain <br />
b.	Run the class com.c123.spring.example.SpringMain <br />
c.	Check the output file (location is printed in the Intellij console) <br /> 
d.	If you still feel confused. Use Intellij Debugger to get a better 
    understanding of the application flow. <br />
## 9.4	Spring Annotations based application
In this lab you are required to fix several files in the application
in order to utilize Spring Annotations. <br />
The following are the list of tasks required for you to do: <br />
a.	Edit the springContextAnnotations.xml file in the Spring Annotations folder and add 
<context:component-scan…> for required missing packages. <br />
b.	Edit com.c123.springAnnotations.example.DAL.FileObjectWriter 
    and fix all missing annotations (Hint: Search for “//TODO:”) <br />
c.	Edit com.c123.springAnnotations.example.UserGenerator 
    and fix all missing annotations (Hint: Search for “//TODO:” <br />
d.	Run com.c123.springAnnotations.example.SpringAnnotationsMain <br />
e.	Check the output file (location is printed in the Intellij console) <br />
f.	You might be required to add import statements for supporting the added annotation.