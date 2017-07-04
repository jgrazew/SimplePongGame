<!DOCTYPE html>
<html>
<head>
    <title></title>
	<meta charset="utf-8" />

    <script src="Scripts/modernizr-2.8.3.js"></script>
    <script src="Scripts/jquery-3.1.1.js"></script>
    <script src="Scripts/jquery-3.1.1.min.js"></script>

    <style>
        body {
            height: 100%;
            width: 100%;
            margin: 0;
            background-color: maroon;
        }

        #container {
            position: relative; /*An element with position: RELATIVE; is positioned relative to its normal position; therefore  the width is 60% relative to its normal width; if didnt have relative it would just do 100% width*/
            /*An element with position: ABSOLUTE; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed)*/
            height: 400px;
            width: 60%;
            margin-left: 20%;
            background-color: dimgray;
            margin-top: 20px;
            overflow: hidden; /*The overflow property specifies what happens if content overflows an element's box.*/
        }

        #ball {
            position: absolute;
            height: 20px;
            width: 20px;
            background-color: white;
            top: 30%; /*For absolutely positioned elements, the TOP property sets the bottom edge of an element to a unit above/below the bottom edge of its nearest positioned ancestor*/
            left: 60%;
        }

        .paddle {
            position: absolute;
            height: 20px;
            width: 150px;
            background-color: white;
            left: 40%; /*both start at same center in the beginning of game*/
        }

        #paddle_1 {
            bottom: 0; /*For absolutely positioned elements, the BOTTOM property sets the bottom edge of an element to a unit above/below the bottom edge of its nearest positioned ancestor*/
        }

        #paddle_2 {
            top: 0;
        }

        #restart_div {
            position: absolute;
            height: 100%;
            width: 100%;
            background-color: mediumpurple;
            color: white;
            font-family: sans-serif;
            font-size: 40px;
            text-align: center; /*where text inside div will be*/
            display: none; /*dont want to display until the game is going to get reset*/
        }

        #restart {
            border: none;
            padding: 25px; /*will make button bigger because expands the border so its 25px away from text*/
            font-size: 30px;
        }
    </style>
</head>
<body>
    <div id="container">                <!--the ball, button are relative to the container (see css explanation above)-->
        <div id="ball"></div>
        <div id="paddle_1" class="paddle"></div>
        <div id="paddle_2" class="paddle"></div>
        <div id="restart_div">
            <p id="winner"></p>
            <button id="restart_btn">Restart</button>   <!--button tag displays buttton- can use onclick attribute or JQuery for the click-->
        </div>
    </div>

    <script type="text/javascript">
        //shortcut for below is $(function () {});
        $(document).ready(function () {

            var anim_id;

            //saving dom objects to variables; i thnk these are jQuery objects because of the dollar sign
            var container = $('#container');            
            var ball = $('#ball');
            var paddle = $('.paddle');
            var paddle_1 = $('#paddle_1');
            var paddle_2 = $('#paddle_2');
            var restart_btn = $('#restart');
            var restart_div = $('#restart_div');
            var who_won = $('#winner');

            //saving some initital setup; The parseInt() function parses a String and returns an Integer
            var container_width = parseInt(container.width());
            var container_height = parseInt(container.height());
            var paddle_width = parseInt(paddle.width());
            var ball_height = parseInt(ball.height());
            var ball_width = parseInt(ball.width());

            //some other declarations

            //when game is over will be set to true
            var game_over = false;

            //forreceiving these positions
            var ball_center;
            var paddle_center;

            var ball_go = 'down';
            var ball_right_left = 'right';

            var top = 6;
            var right_left_angle = 0;

            //controls for each paddle
            var move_right_p1 = false;
            var move_left_p1 = false;

            var move_right_p2 = false;
            var move_left_p2 = false;

            var who_won;

            /*----------Game code starts here----------*/

            //The .ready() method offers a way to run JavaScript code as soon as the page's Document Object Model (DOM) becomes safe to manipulate. This will often be a good time to perform tasks that are needed before the 
            //user views or interacts with the page
            //The .on() method is used because you might have a dynamically generated elements (for example coming from an AJAX call), Event handlers are bound only to the currently selected elements; they must exist at 
            //the time your code makes the call to .on() but the actual data might not be filled to later

            //keydown fucntion
            $(document).on('keydown', function (e) {
                //keyCode grabs a code for the key pressed; 37 is for the left key
                var key = e.keyCode;
                //requestAnimationFrame is used in javascript for animtation; then we must define left_p1
                if (key == 37 && move_left_p1 == false) {
                    move_left_p1 = requestAnimationFrame(left_p1);
                } else if (key == 39 && move_right_p1 == false) {
                    move_right_p1 = requestAnimationFrame(right_p1);
                }
                else if (key == 65 && move_left_p2 == false) {
                    move_left_p2 = requestAnimationFrame(left_p2);
                }
                else if (key == 83 && move_right_p2 == false) {
                    move_right_p2 = requestAnimationFrame(right_p2);
                }
                });

            //keyup function
            $(document).on('keyup', function (e) {
                //keyCode grabs a code for the key pressed; 37 is for the left key
                var key = e.keyCode;
                console.log("test");
                console.log(key);
                //requestAnimationFrame is used in javascript for animtation; then we must define left_p1
                if (key == 37) {
                    cancelAnimationFrame(move_left_p1); //cancel frame that key== 37 is assigned to and set move_left_p1 to false that the condition in if statement is true next time in the keydown funtion
                    move_left_p1 = false;
                } else if (key == 39) {
                    cancelAnimationFrame(move_right_p1); //cancel frame that key== 37 is assigned to and set move_left_p1 to false that the condition in if statement is true next time in the keydown funtion
                    move_right_p1 = false;
                }
                else if (key == 65) {
                    cancelAnimationFrame(move_left_p2); 
                    move_left_p2 = false;
                } else if (key == 83) {
                    cancelAnimationFrame(move_right_p2); 
                    move_right_p2 = false;
                }
            });

            //below parseInt is used often and I have a reference email about this. But some methods in javascript automatically return a string therefor the + (sum) would do a concatenation. Therefore parseInt is used often here
            //    to avoid the concatenation

            function left_p1() {
                //check to see if x axis has passed the Absolute Left (you can make 100% width and 100% height by using top: 0; left: 0; bottom: 0; right: 0;
                if(parseInt(paddle_1.css('left')) > 0) {
                //left will be: parseInt(paddle_1.css('left')) - 15
                paddle_1.css('left', parseInt(paddle_1.css('left')) - 15);
                move_left_p1 = requestAnimationFrame(left_p1); //place inside so that it will become recursive and call again and again; SEE EXPLANATION AT THE BTTOM FOR CLARIFICATION ON THE RECURSIVE CALL
                }
            }

            function right_p1() {
                //check to see if x axis has passed the Absolute Right but there is no '0' for this therefore we have to take the containers width and subtract the paddle
                if (parseInt(paddle_1.css('left')) < container_width - paddle_width) {
                    //since we are now moving right we want to increase our left attribute therefore we are adding
                    paddle_1.css('left', parseInt(paddle_1.css('left')) + 15);
                    move_right_p1 = requestAnimationFrame(right_p1);  //place inside so that it will become recursive and call again and again; SEE EXPLANATION AT THE BTTOM FOR CLARIFICATION ON THE RECURSIVE CALL
                }
            }

            function left_p2() {
                if (parseInt(paddle_2.css('left')) > 0) {
                    paddle_2.css('left', parseInt(paddle_2.css('left')) - 15);
                    move_left_p2 = requestAnimationFrame(left_p2); 
                }
            }

            function right_p2() {
                if (parseInt(paddle_2.css('left')) < container_width - paddle_width) {
                    paddle_2.css('left', parseInt(paddle_2.css('left')) + 15);
                    move_right_p2 = requestAnimationFrame(right_p2);  
                }
            }

            /*---------Ball Control Starts Here--------*/

            anim_id = requestAnimationFrame(repeat);

            function repeat() {
                //below was added after the the if else right before the function ends

                if (game_over == false) {
                    if (collision(ball, paddle_1)) {
                        //retrieves center of ball and paddle below that will be used so that ball goes at angle when coming off the paddle; added for the else if too for paddle_2 below
                        ball_center = parseInt(ball.css('left')) + ball_width / 2;
                        paddle_center = parseInt(paddle_1.css('left')) + paddle_width / 2;
                        //if ball center is greater than paddle center than we move the ball to the right else the ball goes to the left; will make go right or left by increasing/ decreasing the value of the balls css left attribute
                        ball_right_left = (ball_center > paddle_center ? 'right' : 'left');
                        //value below will be used to change the css left; note if do not use parseInt you will not get the number that you are expecting to get; WITHOUT dividing by 6 our angles will be something like 20 - 40 which
                        //is to sharp for our game
                        right_left_angle = parseInt(Math.abs(paddle_center - ball_center) / 6);
                        ball_go = 'up';
                    } else if (collision(ball, paddle_2)) {
                        ball_center = parseInt(ball.css('left')) + ball_width / 2;
                        paddle_center = parseInt(paddle_2.css('left')) + paddle_width / 2;
                        ball_right_left = (ball_center > paddle_center ? 'right' : 'left');
                        right_left_angle = parseInt(Math.abs(paddle_center - ball_center) / 6);
                        ball_go = 'down';
                    } else if (parseInt(ball.css('left')) <= 0) {
                        //if left attribute hits left wall then make the ball go right
                        ball_right_left = 'right';
                    } else if (parseInt(ball.css('left')) >= container_width - ball_width) {
                        ball_right_left = 'left';
                    } else if (parseInt(ball.css('top')) <= 0) {
                        who_won = 'Player 1';
                        stop_the_game();
                        console.log("test2")
                    } else if (parseInt(ball.css('top')) >= container_height - ball_height) {
                        who_won = 'Player 2';
                        stop_the_game();
                        console.log("test3")
                    }

                    if (ball_go == 'down') {
                        ball_down();
                    } else {
                        ball_up();
                    }

                    anim_id = requestAnimationFrame(repeat);

                }

            }
            
            //function will be used to bring down the ball which means increase the css top; top is a variable declared with the other declarations above; ball_go INITIALLY SET TO 'down' THEREFORE WILL START WITH DOWN
            function ball_down() {
                ball.css('top', parseInt(ball.css('top')) + top);
                if (ball_right_left == 'right') {
                    //below we are adding b/c we are moving right therefore we want to increase the left css to move further away
                    ball.css('left', parseInt(ball.css('left')) + right_left_angle);
                } else {
                    //if not right then we are moving left and we want ball to be closer to the left therefore we eant to decrease the left
                    ball.css('left', parseInt(ball.css('left')) - right_left_angle);
                }
            }

            //if we want ball to go up then we decrease the top
            function ball_up() {
                ball.css('top', parseInt(ball.css('top')) - top);
                if (ball_right_left == 'right') {
                    //below we are adding b/c we are moving right therefore we want to increase the left css to move further away
                    ball.css('left', parseInt(ball.css('left')) + right_left_angle);
                } else {
                    //if not right then we are moving left and we want ball to be closer to the left therefore we eant to decrease the left
                    ball.css('left', parseInt(ball.css('left')) - right_left_angle);
                }
            }
             
            //note that if we got rid of the restart.slideDown() below the game would be over but we would still be able to move the paddle; to fix this just wrap logic in $(document).on('keydown', function (e) { if(game_over==false){...}};-----then we must add a cancelAnimationFrame(move_right_p1); for left and right of paddle 1 and 2 (also do this in the stop_the_game() function            
            function stop_the_game() {
                game_over = true;
                cancelAnimationFrame(anim_id);
                $('#winner').html(who_won + 'won the game');
                restart_div.slideDown();
                console.log('test');
            }

            //location.reload() refreshes the page- note that i dont think that it can go into document.ready()
            $('#restart_btn').click(function () {
                location.reload();
                console.log("restart");
            })
            
            

            /*---------Game code ends here------------*/



            //below is for how the ball and paddle interact with each other; STUDY THESE INTERACTIONS

            //The .offset() method allows us to retrieve the current position of an element (specifically its border box, which excludes margins) relative to the document; .offset() returns an object containing the properties top and left
            //the outerheight() function- Get the current computed outer height (including padding, border, and optionally margin) for the first element in the set of matched elements or set the outer height of every matched element. it is outerHeight(false by default). outerHeight(true) function returns the total height of the element including padding border and margins; 

            function collision($div1, $div2) {      //div1 will be a ball and div2 a paddle when function is called
                var x1 = $div1.offset().left;
                var y1 = $div1.offset().top;            //current position with in border box
                var h1 = $div1.outerHeight(true);       //since includes true which returns the total height of the element including padding border and margins
                var w1 = $div1.outerWidth(true);
                var b1 = y1 + h1;
                var r1 = x1 + w1;
                var x2 = $div2.offset().left;
                var y2 = $div2.offset().top;
                var h2 = $div2.outerHeight(true);
                var w2 = $div2.outerWidth(true);
                var b2 = y2 + h2;
                var r2 = x2 + w2;

                if (b1 < y2 || y1 > b2 || r1 < x2 || x1 > r2) return false; //if balls position is less than the paddles position than the ball passed the paddle
                return true;
            }

        });

    </script>
</body>
</html>

<!--[move_left_p1 = requestAnimationFrame(left_p1);] calls  [function left_p1()] which moves the css of [paddle_1] then makes a recursive call to itself just as you did in the first part of this line 
[move_left_p1 = requestAnimationFrame(left_p1);] so since this was caalled on the event of 'keydown' as long as you hold the buttton down the other function on the event 'keyup' is never called
as soon as you lift your finger up the function is not called anymore this is the reason why it doesnt keep moving after you lift your finger up-->
