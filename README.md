# WatsonAssistant-Integrate-with-a-website

Previously I created the control panel page, so I added the Watson Assistant

#This code for my watson assistant: 

      <script>
      window.watsonAssistantChatOptions = {
      integrationID: "dd956bf9-97be-4f71-9b3f-eb24ae34cade", // The ID of this integration.
      region: "eu-gb", // The region your integration is hosted in.
      serviceInstanceID: "12dba3ba-f59c-49f3-99a7-2c3009172491", // The ID of your service instance.
      onLoad: function(instance) { instance.render(); }
    };
    setTimeout(function(){
    const t=document.createElement('script');
    t.src="https://web-chat.global.assistant.watson.appdomain.cloud/loadWatsonAssistantChat.js";
    document.head.appendChild(t);
    });
    </script>
    
    
#HTML file : 
Start with the basic structure which is: the head and body inside HTML tag

Then the title as we see: 

      <title>Control Panel</title>

Then the code that links between the HTML file and CSS file 

      <link rel="stylesheet" href="style2.css">

Then the form that has the directions buttons [ left, right, forward, backward, and stop ] 

      <h1>Control Panel</h1>
      <form action="" name="form1" method="post">
      <div class="middle">
      <button type="submit" name="left" class="btn btn1">left</button>
      <button type="submit" name="right" class="btn btn2">right</button>
      <button type="submit" name="forward" class="btn btn3">forward</button>
      <button type="submit" name="backward" class="btn btn4">backward</button>
      <button type="submit" name="stop" class="btn btn5">stop</button>
      </div>
      </form>


#CSS file: 

These code for the body and the picture on it and the position: 

      body{
      margin: 0;
      padding: 0;
             background-image: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)), url('p1.jpg');
      background-size: cover;
      background-repeat: no-repeat;	
      background-attachment: fixed;
      color: #FFFFFF; 
      }

      h1{
      font-size: 3rem;
      text-align: center;
      margin: 7rem 150;
      font-family: "montserrar", sans-serif;
      color: #FFFFFF;
      }
      .middle{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;	
      }

These codes to style the buttons: 

      .btn{
      background: none;
      border: 2px solid #4C9900;
      font-family: "montserrar", sans-serif;
      text-transform: uppercase;
      padding: 12px 20px;
      min-width: 200px;
      margin: 10px;
      cursor: pointer;
      transition: color 0.4s linear;
      position: relative;
      color: #4C9900;	
      }
      .btn5{
      color: #000000;		
      }

These code to style the hover of buttons : 

      .btn:hover{
      color: #fff;
      }
      .btn::before{
      content:"";
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: #4C9900;
      z-index: -1;
      transition: transform 0.5s;
      transform-origin: 0 0;
      transition-timing-function: cubic-bezier(0.5,1.6,0.4,0.7);
      }
      .btn1::before{
      transform: scaleX(0);
      }
      .btn3::before{
      transform: scaleY(0);
      }
      .btn1:hover::before{
      transform: scaleX(1);	
      }
      .btn3:hover::before{
      transform: scaleY(1);	
      }


      .btn2::before{
      transform: scaleX(0);
      }
      .btn4::before{
      transform: scaleY(0);
      }
      .btn2:hover::before{
      transform: scaleX(1);	
      }
      .btn4:hover::before{
      transform: scaleY(1);	
      }

      .btn5::before{
      transform: scale(1);
      }
      .btn5:hover::before{
      transform: scale(1);	
      }


#p1 picture is necessary to upload to fix the style of the HTML file and CSS file.

    
    
