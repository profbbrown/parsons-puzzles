<html>
    <head>Area.c</head>
    <body>
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "#include &lt;stdio.h&gt;\n" +
    "int main()\n" +
    "{\n" +
    "    int height, width, area;\n" +
    "    printf(\"Enter height of the rectangle: \");\n" +
    "    scanf(\"%d\", &height);\n" +
    "    printf(\"Enter width: \");\n" +
    "    scanf(\"%d\", width);\n" +
    "    area = heigh * width;\n" +
    "    printf(\"Area: %d&#92;n\", area);\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
    </body>
    </html>
