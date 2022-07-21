# Task1 (IOT)


**HTML**
_use definition in HTML for declration:_

<!DOCTYPE html>
<html>
<head>
<title>Title of the document</title>
  <style>
  </style>
</head>

<body>
  <script>
  </script>
</body>
  
</html>

**body part**
_in this part of HTML incloudes javascript and basic design_

  basic design such as:
  1.text
  2.button
  3.textarea
  
  <div class="voice_to_text">
    <h1>convert speech to text</h1>
     <textarea id="convert_text" rows="6" cols="50"></textarea>
  </br>
    <button id="click_to_convert" >start</button>
  </br>
  </br>
     press the start button to start
   </div>
   
*Note : use command </br> To go to the new line

   
**javascript part**

*use <script></script> and write the program between thim:
 
 <script>
        
      click_to_convert.addEventListener('click', function(){
    var speech = true;
    window.SpeechRecognition = window.webkitSpeechRecognition;
   const recognition =new SpeechRecognition();
   recognition.interimResults = true;
   
   recognition.addEventListener('result', e=>{
   const transcript = Array.from(e.results)
   .map(result => result[0])
   .map(result => result.transcript)
   
   convert_text.innerHTML = transcript;
   })
   recognition.lang="ar";
   if(speech == true){
   recognition.start();
   }
  
})

    </script>
    
    
 *The command **recognition.lang="ar";** use for select the Arabic language.
 
 
 
 
 
 
 
 
 

