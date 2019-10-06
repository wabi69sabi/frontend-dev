---
layout: null
---

{::nomarkdown}
<html>
    <head>
            <title>Tic Tac Toe</title>
        <script type="text/javascript">
            var board = new Array(9);    //Simulate the board

            for(i=0;i<9;i++)      //Assign different values to each position
            {
                board[i]=i;
            }
            var occupiedSquares = 0;    //A placeholder for checking for Cat's Game
            var Xwins = 0;
            var Owins = 0;
            var Cat = 0;

            function printX0() {        //Redo print X or O and check for win!
                document.getElementById("position0").innerHTML = "X";
                checkForWin(0,9);
            }
            function printO0() {
                document.getElementById("position0").innerHTML = "O";
                checkForWin(0,10);
            }
            function printX1() {
                document.getElementById("position1").innerHTML = "X";
                checkForWin(1,9);
            }
            function printO1() {
                document.getElementById("position1").innerHTML = "O";
                checkForWin(1,10);
            }
            function printX2() {
                document.getElementById("position2").innerHTML = "X";
                checkForWin(2,9);
            }
            function printO2() {
                document.getElementById("position2").innerHTML = "O";
                checkForWin(2,10)
            }
            function printX3() {
                document.getElementById("position3").innerHTML = "X";
                checkForWin(3,9);
            }
            function printO3() {
                document.getElementById("position3").innerHTML = "O";
                checkForWin(3,10);
            }
            function printX4() {
                document.getElementById("position4").innerHTML = "X";
                checkForWin(4,9);
            }
            function printO4() {
                document.getElementById("position4").innerHTML = "O";
                checkForWin(4,10);
            }
            function printX5() {
                document.getElementById("position5").innerHTML = "X";
                checkForWin(5,9);
            }
            function printO5() {
                document.getElementById("position5").innerHTML = "O";
                checkForWin(5,10);
            }
            function printX6() {
                document.getElementById("position6").innerHTML = "X";
                checkForWin(6,9);
            }
            function printO6() {
                document.getElementById("position6").innerHTML = "O";
                checkForWin(6,10);
            }
            function printX7() {
                document.getElementById("position7").innerHTML = "X";
                checkForWin(7,9);
            }
            function printO7() {
                document.getElementById("position7").innerHTML = "O";
                checkForWin(7,10);
            }
            function printX8() {
                document.getElementById("position8").innerHTML = "X";
                checkForWin(8,9);
            }
            function printO8() {
                document.getElementById("position8").innerHTML = "O";
                checkForWin(8,10);
            }

            function ClearBoard() {         //Reset the board physically.
                 document.getElementById("position0").style.backgroundColor = "black";
                 document.getElementById("position0").innerHTML = "<button type = 'button' name = 'pos0X' onclick = printX0();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos0O' onclick = printO0();>O</button>";

                 document.getElementById("position1").style.backgroundColor = "black";
                 document.getElementById("position1").innerHTML = "<button type = 'button' name = 'pos1X' onclick = printX1();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos1O' onclick = printO1();>O</button>";

                 document.getElementById("position2").style.backgroundColor = "black";
                 document.getElementById("position2").innerHTML = "<button type = 'button' name = 'pos2X' onclick = printX2();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos2O' onclick = printO2();>O</button>";

                 document.getElementById("position3").style.backgroundColor = "black";
                 document.getElementById("position3").innerHTML = "<button type = 'button' name = 'pos3X' onclick = printX3();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos3O' onclick = printO3();>O</button>";

                 document.getElementById("position4").style.backgroundColor = "black";
                 document.getElementById("position4").innerHTML = "<button type = 'button' name = 'pos4X' onclick = printX4();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos4O' onclick = printO4();>O</button>";

                 document.getElementById("position5").style.backgroundColor = "black";
                 document.getElementById("position5").innerHTML = "<button type = 'button' name = 'pos5X' onclick = printX5();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos5O' onclick = printO5();>O</button>";

                 document.getElementById("position6").style.backgroundColor = "black";
                 document.getElementById("position6").innerHTML = "<button type = 'button' name = 'pos6X' onclick = printX6();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos6O' onclick = printO6();>O</button>";

                 document.getElementById("position7").style.backgroundColor = "black";
                 document.getElementById("position7").innerHTML = "<button type = 'button' name = 'pos7X' onclick = printX7();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos7O' onclick = printO7();>O</button>";

                 document.getElementById("position8").style.backgroundColor = "black";
                 document.getElementById("position8").innerHTML = "<button type = 'button' name = 'pos8X' onclick = printX8();>X</button>"
                 + "   " + "<button type = 'button' name = 'pos8O' onclick = printO8();>O</button>";

            }

            function Reset() {            
                 document.getElementById("Scoreboard").innerHTML = 'Wins for X: ' + Xwins + "<br/>"  //Update the Scoreboard
                + 'Wins for O: ' + Owins + "<br/>" + 'Cats Game:  ' + Cat;
                for(j=0;j<9;j++)      //Reset the board virtually.
                {
                board[j]=j;
                }
                occupiedSquares=0;   //Reset to 0 occupied squares.         
            }

            function checkForWin(pos,value) {
                board[pos]=value;       //The position is given a value of 9 for X, 10 for O.
                occupiedSquares++;      //When a square is chosen, it is counted.

                    if (board[0]==board[1] && board[0]==board[2]) {
                        document.getElementById("position0").style.backgroundColor="green";
                        document.getElementById("position1").style.backgroundColor="green";
                        document.getElementById("position2").style.backgroundColor="green";
                        if (document.getElementById("position0").innerHTML=="X")
                        Xwins++;
                        else                         
                        Owins++;
                        Reset();  //Update Scoreboard immediately upon a decision.
                    } else
                    if (board[3]==board[4] && board[3]==board[5]) {
                        document.getElementById("position3").style.backgroundColor="green";
                        document.getElementById("position4").style.backgroundColor="green";
                        document.getElementById("position5").style.backgroundColor="green";
                        if (document.getElementById("position3").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[6]==board[7] && board[6]==board[8]) {
                        document.getElementById("position6").style.backgroundColor="green";
                        document.getElementById("position7").style.backgroundColor="green";
                        document.getElementById("position8").style.backgroundColor="green";
                        if (document.getElementById("position6").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[0]==board[3] && board[0]==board[6]) {
                        document.getElementById("position0").style.backgroundColor="green";
                        document.getElementById("position3").style.backgroundColor="green";
                        document.getElementById("position6").style.backgroundColor="green";
                        if (document.getElementById("position0").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[1]==board[4] && board[1]==board[7]) {
                        document.getElementById("position1").style.backgroundColor="green";
                        document.getElementById("position4").style.backgroundColor="green";
                        document.getElementById("position7").style.backgroundColor="green";
                        if (document.getElementById("position1").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[2]==board[5] && board[2]==board[8]) {
                        document.getElementById("position2").style.backgroundColor="green";
                        document.getElementById("position5").style.backgroundColor="green";
                        document.getElementById("position8").style.backgroundColor="green";
                        if (document.getElementById("position2").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[0]==board[4] && board[0]==board[8]) {
                        document.getElementById("position0").style.backgroundColor="green";
                        document.getElementById("position4").style.backgroundColor="green";
                        document.getElementById("position8").style.backgroundColor="green";
                        if (document.getElementById("position0").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (board[2]==board[4] && board[2]==board[6]) {
                        document.getElementById("position2").style.backgroundColor="green";
                        document.getElementById("position4").style.backgroundColor="green";
                        document.getElementById("position6").style.backgroundColor="green";
                        if (document.getElementById("position2").innerHTML=="X")
                        Xwins++;
                        else
                        Owins++;
                        Reset();
                    } else
                    if (occupiedSquares == 9) { //Are all squares occupied with no winner?
                        document.getElementById("position0").style.backgroundColor="red";
                        document.getElementById("position1").style.backgroundColor="red";
                        document.getElementById("position2").style.backgroundColor="red";
                        document.getElementById("position3").style.backgroundColor="red";
                        document.getElementById("position4").style.backgroundColor="red";
                        document.getElementById("position5").style.backgroundColor="red";
                        document.getElementById("position6").style.backgroundColor="red";
                        document.getElementById("position7").style.backgroundColor="red";
                        document.getElementById("position8").style.backgroundColor="red";
                        Cat++;
                        Reset();
                    }
            }
        </script>
       <style type="text/css">  
       button {
           background-color: gray;
           font-weight: bold;
       }    
       #position0 {
            left: 200px;
            top: 100px;
            margin-right: 10px;
            margin-bottom: 10px;
            background-color: black;
        }
        #position1 {
            left: 400px;
            top: 100px;
            background-color: black;
        }
        #position2 {
            left: 600px;
            top: 100px;
            background-color: black;
        }
        #position3 {
            left: 200px;
            top: 300px;
            background-color: black;
        }
        #position4 {
            left: 400px;
            top: 300px;
            background-color: black;
        }
        #position5 {
            left: 600px;
            top: 300px;
            background-color: black;
        }
        #position6 {
            left: 200px;
            top: 500px;
            background-color: black;
        }
        #position7 {
            left: 400px;
            top: 500px;
            background-color: black;
        }
        #position8 {
            left: 600px;
            top: 500px;
            background-color: black;
        }
        #Scoreboard {
            position: absolute;
            border: 2px solid orangered;
            top: 60px;
            left: 900px;
            font-size: 40px;
            width: 300px;
            height: 200px;
            text-align: center;
            padding-top: 30px;
            background-color: black;
            color: orangered;
        }
        div {
            position: absolute;          
            width: 199px;
            height: 199px;  
            color: orangered;
            text-align: center;
            font-size: 180px;
            <!-- border: 2px solid orangered; -->
            overflow: hidden;
        }
        .with-border {
          border: 2px solid orangered;
        }
        .clear-board {
          z-index: 1;
        }
        #dm-extension-sniffer {
          z-index: -1;
        }
        #footer {
          padding: 20px;
        }
        </style>
    </head>
    <body>
        <h1>Tic-Tac-Toe!</h1>
        <button class="clear-board" type="button" name="NewGame"
        onclick="ClearBoard();">New Game</button>

        <p id=Scoreboard>
            Wins for X: 0
            <br/>
            Wins for O: 0
            <br/>
            Cats Game: 0
        </p>
        <div class='with-border' id=position0>
            <button type="button" name="pos0X"
            onclick="document.getElementById('position0').innerHTML='X';checkForWin(0,9);">X</button>
            <button type="button" name="pos0O"
            onclick="document.getElementById('position0').innerHTML='O';checkForWin(0,10);">O</button>           
        </div>
        <div class='with-border' id=position1>
            <button type="button" name="pos1X"
            onclick="document.getElementById('position1').innerHTML='X';checkForWin(1,9);">X</button>
            <button type="button" name="pos1O"
            onclick="document.getElementById('position1').innerHTML='O';checkForWin(1,10);">O</button>        
        </div>
        <div class='with-border' id=position2>
            <button type="button" name="pos2X"
            onclick="document.getElementById('position2').innerHTML='X';checkForWin(2,9);">X</button>
            <button type="button" name="pos2O"
            onclick="document.getElementById('position2').innerHTML='O';checkForWin(2,10);">O</button>          
        </div>
        <div class='with-border' id=position3>
            <button type="button" name="pos3X"
            onclick="document.getElementById('position3').innerHTML='X';checkForWin(3,9);">X</button>
            <button type="button" name="pos3O"
            onclick="document.getElementById('position3').innerHTML='O';checkForWin(3,10);">O</button>
        </div>
        <div class='with-border' id=position4>
            <button type="button" name="pos4X"
            onclick="document.getElementById('position4').innerHTML='X';checkForWin(4,9);">X</button>
            <button type="button" name="pos4O"
            onclick="document.getElementById('position4').innerHTML='O';checkForWin(4,10);">O</button>
        </div>
        <div class='with-border' id=position5>
            <button type="button" name="pos5X"
            onclick="document.getElementById('position5').innerHTML='X';checkForWin(5,9);">X</button>
            <button type="button" name="pos5O"
            onclick="document.getElementById('position5').innerHTML='O';checkForWin(5,10);">O</button>
        </div>
        <div class='with-border' id=position6>
            <button type="button" name="pos6X"
            onclick="document.getElementById('position6').innerHTML='X';checkForWin(6,9);">X</button>
            <button type="button" name="pos6O"
            onclick="document.getElementById('position6').innerHTML='O';checkForWin(6,10);">O</button>
        </div>
        <div class='with-border' id=position7>
            <button type="button" name="pos7X"
            onclick="document.getElementById('position7').innerHTML='X';checkForWin(7,9);">X</button>
            <button type="button" name="pos7O"
            onclick="document.getElementById('position7').innerHTML='O';checkForWin(7,10);">O</button>
        </div>
        <div class='with-border' id=position8>     
            <button type="button" name="pos8X"
            onclick="document.getElementById('position8').innerHTML='X';checkForWin(8,9);">X</button>        
            <button type="button" name="pos8O"
            onclick="document.getElementById('position8').innerHTML='O';checkForWin(8,10);">O</button>
        </div>
        <footer id='footer'>&copy; 2019 Kenneth White<footer>
    </body>
</html>
{:/}
