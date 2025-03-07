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
