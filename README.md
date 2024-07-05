# PhotoGalleryRotate

1. This is a javascript exercise to see if I could create an image gallery and change the images by clicking on a button.
2. This version assumes 5 images named "pic1.jpg", "pic2.jpg", etc.
3. An updated version should allow any number of pics in the gallery so the for loops might for example use array.length to figure out the size.
4. The only "trick" in this project was figuring out how to use text (e.g., "pic1.jpg") as a file object instead of as a string.  There are several ways to do this but I opted for an easy way by returning "innerHTML = `<img src=${filename} />` using backticks.  I put this in a "rotate" function and used the onclick event listener when the button is pressed.
5. Here is the original code for index.html:
      <!DOCTYPE html>
      <html>
      <head>
      <title>rotate images</title>
      <!--butterfly photos courtesy of https://www.publicdomainpictures.net/ -->
      <link rel='stylesheet' type='text/css' href="styles.css" />
      </head>
      	
      <body>
      <div id="div1">Butterfly</div>
      <button id="btn1" onclick=rotor();>Change Me</button>
      <script src = "app.js"></script>
      </body>
      </html>
6. Here is the code for the css and javascript files (Using "var" in the count declaration should be replaced by moving the variable in the code and using "let".  I rough coded this app to see if it would work.  Future versions would clean up the code as well as add features).
   #Javascript:
    let diver = document.getElementById('div1');
    diver.innerHTML="Hello";
    const gala = [];
    let imgx = "";
    let picto = [];
    function rotor(){
    	for(var count = 1; count <6; count++){
    		imgx = "pic" + count + ".jpg";
    		gala.push(imgx);
    	    }
    	document.getElementById('div1').innerHTML = `<img src="./images/${gala.shift()}"/>`;
    }
  #CSS
    img{
    width:130px;
    height:130px;
    }
   
