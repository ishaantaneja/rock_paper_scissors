Rock Paper Scissor Game

Find the logic return below

let options = ["rock", "paper", "scissor"];
let stat = document.getElementById("winner");

const computerOption = () => {
return randomSelect(options);
};

function randomSelect(arr) {
let randomIndex = Math.floor(Math.random()\*arr.length);
return arr[randomIndex];
}

rockButton = document.getElementById("rock");
scissorButton = document.getElementById("scissor");
paperButton = document.getElementById("paper");

buttons = []
buttons[0] = rockButton;
buttons[1] = scissorButton;
buttons[2] = paperButton;

buttons.forEach(button => {
button.addEventListener("click", () => {
computerReturnedOption = computerOption();

        if (computerReturnedOption === "rock" && button.innerText.toLowerCase() === "paper"){
            stat.innerText = "Winner is User" + " Computer chose " + computerReturnedOption;
        } else if (computerReturnedOption === "rock" && button.innerText.toLowerCase() === "scissor"){
            stat.innerText = "Winner is Computer" + " Computer chose " + computerReturnedOption;
        } else if (computerReturnedOption === "scissor" && button.innerText.toLowerCase() === "paper"){
            stat.innerText = "Winner is Computer" + " Computer chose " + computerReturnedOption;
        } else if (computerReturnedOption === "scissor" && button.innerText.toLowerCase() === "rock") {
            stat.innerText = "Winner is User" + " Computer chose " + computerReturnedOption;
        } else if (computerReturnedOption === "paper" && button.innerText.toLowerCase() === "scissor") {
            stat.innerText = "Winner is User" + " Computer chose " + computerReturnedOption;
        } else if (computerReturnedOption === "paper" && button.innerText.toLowerCase() === "rock") {
            stat.innerText = "Winner is Computer"  + " Computer chose " + computerReturnedOption;
        } else if(computerReturnedOption === button.innerText.toLowerCase()) {
            stat.innerText = "Draw" + " Computer chose " + computerReturnedOption;
        }


});
});
