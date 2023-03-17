This Project is for loading variable values from specific files directly and also using shared library.

1. Loading directly from file:
    
    Add a line in jenkinsfile to load the file:-
    
      data = load "variable-doc"
      
    we can use the varibles in variable-doc file by $VARIBLE_NAME.
    
    Example,  $CITY
              $AGE
              
2. Using a shared-library:
      File has to be under src and the file has to write as shown in the src/com/org/re/Constants.groovy
      
      
      import the file from shared library as below in jenkinsfile
      
            @Library('shared-library') _        #has to configure the shared-library. FOllow the doc from jenkins page.
            import com.org.re.Constants

      Now, we can use the variable as ${Constants.LAST_NAME}
