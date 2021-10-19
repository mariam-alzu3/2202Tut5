let nextPlayer = 'X'; // takes a value of either 'X' or 'O' according to the game turns

//initialize the game
/*
var intilization = document.createElement('button');
intilization.innerText = 'Start Game!';
document.getElementById('game-over-lbl').appendChild(intilization);
intilization.addEventListener('click', (intialEvent) => {intialEvent.target.hidden = true} )
// use the value stored in the nextPlayer variable to indicate who the next player is
*/

let playerIndicator1 = document.createTextNode(nextPlayer);
document.getElementById('next-lbl').appendChild(playerIndicator1);


//This call will create the buttons needed for the gameboard.
let playerIndicator = document.querySelector('b');
let playerText = 'Next Player';
playerIndicator.innerText = playerText;
createGameBoard()

function createGameBoard()
{
    // Programatically add a button with square brackets enclosing an empty space to each cell in the gameboard
    for(let i = 0; i < 9; i++){
        let cellID = 'c' + (i+1);
        var newBtn = document.createElement('button');
        newBtn.setAttribute('id', 'b' + i);
        document.getElementById(cellID).appendChild(newBtn).innerHTML = "[ &nbsp ]" ;
    }
   
}

// Programatically add 'takeCell' as an event listener to all the buttons on the board

let btns = document.querySelectorAll('button');
for (let i=0; i<btns.length; i++)
{
    btns[i].addEventListener('click', (event) => { takeCell(event)});
}

var butonCount = 0;
// This function will be used to respond to a click event on any of the board buttons.
function takeCell(event)
{
    //alert("edit buttn was clicked");

    /*
        When the button is clicked, the space inside its square brackets is replaced by the value in the nextPlayer before switching it
    */
        let clickedBtn = event.target.id;
        document.getElementById(clickedBtn).innerHTML = nextPlayer;

        document.getElementById(clickedBtn).disabled = true;

        if(nextPlayer == 'X'){
            nextPlayer = 'O';
        }
        else if (nextPlayer == 'O'){
            nextPlayer = 'X';
        }


        playerIndicator1.remove();
        playerIndicator1 = document.createTextNode(nextPlayer);
        document.getElementById('next-lbl').appendChild(playerIndicator1);


        butonCount++;        


    // Make sure the button is clickable only once (I didn't mention how to do that, look it up :) )

    // Check if the game is over
    if (isGameOver())
    {
        // let the lable with the id 'game-over-lbl' display the words 'Game Over' inside <h1> element
        let lbl = document.getElementById('game-over-lbl');
        var Header = document.createElement('h1');
        Header.innerText = 'Game Over!';
        lbl.appendChild(Header);
    }

    // I'll leave declaring the winner for your intrinsic motivation, it's not required for this assignment 
}

function isGameOver()
{
    // This function returns true if all the buttons are disabled and false otherwise 
    if(butonCount == 9){
        return true;
    }
    else {
        return false;
    }
   
}
