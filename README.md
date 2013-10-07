Form-validation
=============

A easy form validation with jquery, that is very readable and easy to remember because of the nearly spoken code.

```
var name = $('#name')
,   email = $('#email')
,   age = $('#age');

$('#submit').click(function(){
  var noErrors = validate();
  if(noErrors){
    // Submit function
  }
});

function validate() {
  var are = new smartValidate();
  are(name).empty().addClass('error');
  are(email).empty().and().notIncluding('@').addClass('error');
  are(age).empty().and().notaNumber().addClass('error');
  
  return are.there.errors; // returns true or false
}
```
