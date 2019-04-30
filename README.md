# table-selection-jquery-plugin
Single or Multiple select row and return value from table
<div>
<img alt="preview" src="https://github.com/jounger/table-selection-jquery-plugin/blob/master/preview.png"/>
<h1>How to use?</h1>
  <h3>Setup plugin</h3>
  
  ```
    var $rows = [];
    $(function() {
    	console.log( "ready!" );
        // start plugin
        $('#tableSelected').TableSelection({
                sort : false, // sort or not (true | false)
                status : 'multiple', // single or multiple selection (default is 'single')
            }, function(obj){ // callback function return selected rows array
                $rows = obj.rows;
        });

    });
  ```
  
  <h3>Do something</h3>
  
 ```
    // Get HTML Object from row in array
    function showSelectedRow(array){
        $('#info').empty();
        $.each(array, function(i, row){
            $('#info').append('<li>' 
                + $('#tableSelected').RowValue(row).find('td').eq(2).html() // HTML Object
                + '</li>');
        });
    }
 ```
  
 </div>
