Form-validation
=============

A easy form validation with jquery, that is very readable and easy to remember because of the nearly spoken code.

Features:
- Removes classes that were added automaticly, when the problem is fixed.

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
  var is = new smartValidate();
  is(name).empty().addClass('error');
  is(email).empty().and().notIncluding('@').addClass('error');
  is(age).empty().and().notaNumber().addClass('error');
  
  return are.there.errors; // returns true or false
}
```
