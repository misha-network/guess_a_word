## Welcome to project "guess_a_word"!

Guess a word! is game wherein you required guess a word.

### All Code

Here are all code of project

```markdown
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Guess a word!</title>
</head>
<body>

<h1>Guess a word!</h1>

<script type="text/javascript">
	var words = [
	"javascript",
	"monkey",
	"amazing",
	"pancake",
	"cat",
	"good",
	"tea",
	"cafe",
	"man",
	"women",
	"hello"
	];

	var word = words[Math.floor(Math.random() * words.length)];

	var answerArray = [];
	for (var i = 0; i < word.length; i++) {
		answerArray[i] = "_";
	}

	var remainingLetters = word.length;

	while (remainingLetters > 0) {
		alert(answerArray.join(" "));
		var guess = prompt("Guess a letter, or click Cancel to stop playing.");
		if (guess === null) {
			break;
		}
		else if (guess.length !== 1) {
			alert("Please enter a single letter.");
		}
		else {
			for (var j = 0; j < word.length; j++) {
				if (word[j] === guess) {
					answerArray[j] = guess;
					remainingLetters--;
				}
			}
		}
	}

	alert(answerArray.join(" "));
	alert("Good job! The answer was " + word);
</script>
</body>
</html>
```
