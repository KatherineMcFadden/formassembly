# formassembly
INSTRUCTIONS
Copy and paste this code into the Properties>Custom Code section of the Form Assembly Form Builder and make the code replacements listed below.

1 - Replace the field alias in this line of code ("tfa_2") for a field which will repeat within the repeatable section such as the Application ID:

    $("input[id^='tfa_2']").each(function(i){

2 - Replace the field alias in this line of code ("tfa_5") for the text region where the hyperlink will show:

    var toPopulate = document.getElementById('tfa_5['+i+']');
    
3 - Replace the text in this line of code ("Review") that you want to show in the hyperlink:

    var linkText = document.createTextNode("Review");    

4 - Replace the field alias in this line of code ("tfa_3") for the field containing the prefilled Application Id:

    var applicationId = document.getElementById('tfa_3['+i+']').value;
            
5 - Replace the redirect url in this line of code ("https://www.tfaforms.com/433296?aid=") with the url that you want to redirect the form taker to when they click the hyperlink:

    a.href = "https://www.tfaforms.com/433296?aid=" + applicationId;      
