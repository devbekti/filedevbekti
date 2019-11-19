# filedevbekti
Mangga

//project web loading


<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <meta name="viewport"content="width=device-width, initial-scale=1.0">
        <style>
        	body {
		    margin: 0;
		    padding: 0;
		    font-family: sans-serif;
		}
		.main {
		    position: absolute;
		    top: 5%;
		    left: 5%;
		    bottom: 5%;
		    right: 5%;
		    float: left;
		    overflow: hidden;
		    display: none;
		    transition: 0.5s ease;
		}
		.header {
		    font-family: cursive;
		    letter-spacing: 1px;
		    font-size: 30px;
		    font-weight: 700;
		    color: #4CAF50;
		    border-bottom: 2px solid #4CAF50;
		    width: 100px;
		    padding: 10px;
		}
		.text {
		    position: relative;
		    overflow: hidden;
		    font-size: 14px;
		    line-height: 20px;
		}
		.button {
		    position: relative;
		    padding: 10px;
		    background-color: red;
		    color: #fff;
		    text-transform: uppercase;
		    letter-spacing: 1px;
		    border: none;
		    border-radius: 4px;
		    outline: none;
		}
		.progress-bar {
		    position: absolute;
		    top: 50%;
		    left: 50%;
		    transform: translate(-50%, -50%);
		    transition: 0.5s ease;
		}
		.header-bar {
		    text-align: center;
		    text-transform: uppercase;
		    color: #000;
		    letter-spacing: 1px;
		    font-weight: 100;
		}
		.bar {
		    position: relative;
		    width: 250px;
		    height: 35px;
		    background-color: silver;
		    border-radius: 4px;
		    margin-bottom: 5px;
		    overflow: hidden;
		}
		.value-bar {
		    position: absolute;
		    top: 0;
		    left: 0;
		    width: 1%;
		    height: 100%;
		    background-color: #4CAF50;
		}
		.value {
		    display: block;
		    float: right;
		    font-size: 15px;
		    font-weight: 800;
		    color: #000;
		}
		.btn {
		    position: relative;
		    padding: 10px;
		    width: 80px;
		    border: none;
		    border-radius: 3px;
		    outline: none;
		    background-color: #4CAF50;
		    color: #fff;
		    text-transform: uppercase;
		    letter-spacing: 1px;
		    overflow: hidden;
		}
        </style>
    </head>
    <body>
        <div class="main">
            <h2 class="header"> Web Page </h2>
            <p class="text">
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
            </p>
            <button class="button"> change background </button>
        </div>
        <div class="progress-bar">
            <h2 class="header-bar"> Progress Bar </h2>
            <div class="bar">
                <div class="value-bar"></div>
            </div>
            <span class="value"> 1% </span>
            <button class="btn"> click </button>
        </div>
        <script>
        	/*
			    nama: candra dwi cahyo
			    email: candradwicahyo18@gmail.com
			*/
			window.addEventListener('load', function() {
			    const button = document.getElementsByClassName('button')[0];
			    
			    button.addEventListener('click', function() {
			        const r = Math.round(Math.random() * 255);
			        const g = Math.round(Math.random() * 255);
			        const b = Math.round(Math.random() * 255);
			        
			        document.body.style.backgroundColor = 'rgb('+ r +', '+ g +', '+ b +')';
			        document.body.style.transition = '0.5s ease';
			        
			        this.previousElementSibling.style.color = '#fff';
			        this.previousElementSibling.style.transition = '0.5s ease';
			        
			        this.previousElementSibling.previousElementSibling.style.color = '#fff';
			        this.previousElementSibling.previousElementSibling.style.transition = '0.5s ease';
			    });
			    
			    const btn = document.getElementsByClassName('btn')[0];
			    const valueBar = document.getElementsByClassName('value-bar')[0];
			    
			    btn.addEventListener('click', function() {
			        let width = 1;
			        setInterval(function() {
			            if( width >= 100 ) {
			                clearInterval();
			                btn.parentElement.style.display = 'none';
			                button.parentElement.style.display = 'block';
			            } else {
			                width++;
			                valueBar.style.width = width + '%';
			                btn.previousElementSibling.textContent = width + '%';
			            }
			        }, 10);
			    });
			});
        </script>
    </body>
</html>
