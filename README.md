# CSN-105
Class stuff cause I bored. It is for class participation or something, idk.

# Kanto
The first region

# Sinnoh
My 2nd favorite region

# Unova
My favorite region.

I don't even know what I am doing, this is for class work.

**Corn Muffins are pretty yummy.**
 *POP* 
~~REDACTED~~
~~REDACTED~~
~~REDACTED~~ **Something secret about classifed stuff that have been declassified.**

```
# Simple Number Guessing Game in PowerShell

# Generate a random number between 1 and 100
$randomNumber = Get-Random -Minimum 1 -Maximum 101
$guesses = 0
$gameOver = $false

Write-Host "Welcome to the Number Guessing Game!"
Write-Host "I have selected a random number between 1 and 100."
Write-Host "Try to guess the number!"

# Start the game loop
while (-not $gameOver) {
    $guesses++
    $userGuess = Read-Host "Enter your guess"

    # Check if the guess is a number
    if ($userGuess -as [int]) {
        if ($userGuess -lt $randomNumber) {
            Write-Host "Too low! Try again."
        }
        elseif ($userGuess -gt $randomNumber) {
            Write-Host "Too high! Try again."
        }
        else {
            Write-Host "Congratulations! You guessed the correct number $randomNumber in $guesses attempts."
            $gameOver = $true
        }
    } else {
        Write-Host "Please enter a valid number."
    }
}
```
```
# Rock, Paper, Scissors Game in PowerShell

# Function to display the result of the game
function Get-Winner {
    param (
        [string]$playerChoice,
        [string]$computerChoice
    )

    if ($playerChoice -eq $computerChoice) {
        Write-Host "It's a tie! Both chose $playerChoice."
    }
    elseif (($playerChoice -eq "Rock" -and $computerChoice -eq "Scissors") -or
            ($playerChoice -eq "Scissors" -and $computerChoice -eq "Paper") -or
            ($playerChoice -eq "Paper" -and $computerChoice -eq "Rock")) {
        Write-Host "You win! $playerChoice beats $computerChoice."
    }
    else {
        Write-Host "You lose! $computerChoice beats $playerChoice."
    }
}

# Welcome message
Write-Host "Welcome to Rock, Paper, Scissors!"
Write-Host "Choose one of the following options: Rock, Paper, or Scissors"

# List of available choices
$choices = @("Rock", "Paper", "Scissors")

# Game loop
do {
    # Get the player's choice
    $playerChoice = Read-Host "Enter your choice (Rock, Paper, or Scissors)"

    # Validate the player's choice
    if ($choices -contains $playerChoice) {
        # Generate a random choice for the computer
        $computerChoice = Get-Random -InputObject $choices

        # Display the choices
        Write-Host "You chose $playerChoice"
        Write-Host "The computer chose $computerChoice"

        # Determine and display the winner
        Get-Winner -playerChoice $playerChoice -computerChoice $computerChoice
    }
    else {
        Write-Host "Invalid choice! Please choose Rock, Paper, or Scissors."
    }

    # Ask if the player wants to play again
    $playAgain = Read-Host "Do you want to play again? (yes/no)"
} while ($playAgain -eq "yes")

Write-Host "Thanks for playing! Goodbye!"
```

Used ChatGPT to make a game code for powershell.
