---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
<div id="Binary Search-sortableTrash" class="sortable-code"></div> 
<div id="Binary Search-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Binary Search-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Binary Search-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "book = [&quot;Archaeology&quot;, &quot;Art&quot;, &quot;Biology&quot;, &quot;Chemistry&quot;, &quot;Computing&quot;, &quot;English&quot;, &quot;French&quot;, &quot;Geography&quot;, &quot;History&quot;, &quot;Maths&quot;, &quot;Psychology&quot;]\n" +
    "found = False\n" +
    "left = 0\n" +
    "right = len(book)-1\n" +
    "find = &quot;Geography&quot;\n" +
    "while found == False and left&lt;=right:\n" +
    "    mid = (left+right)//2\n" +
    "    if book[mid]==find:\n" +
    "        found = True\n" +
    "    else:\n" +
    "        if find&gt;book[mid]:\n" +
    "            left=mid+1\n" +
    "        else:\n" +
    "            right=mid-1\n" +
    "if found == True:\n" +
    "	print(&quot;True&quot;)\n" +
    "else:\n" +
    "	print(&quot;False&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Binary Search-sortable",
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
  $("#Binary Search-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Binary Search-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
