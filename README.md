<!DOCTYPE html>
<html>
<head>
	<title>Тест о Кристинке</title>
</head>
<body>
	<h1>Тест о Кристинке</h1>
	<form id="quiz-form">
		<h2>Вопрос 1:</h2>
		<p>Как Кристина стала деканом?</p>
		<label>
			<input type="radio" name="q1" value="a">
			a) Дала в жопу
		</label><br>
		<label>
			<input type="radio" name="q1" value="b">
			b) Взяла в рот
		</label><br>
		<label>
			<input type="radio" name="q1" value="c">
			c) Честным образом путём демакроических выборов
		</label><br><br>

		<h2>Вопрос 2:</h2>
		<p>Что изменилось после назначения Кристины на новую должность?</p>
		<label>
			<input type="radio" name="q2" value="a">
			a) Ничего
		</label><br>
		<label>
			<input type="radio" name="q2" value="b">
			b) Она "зазвездилась"
		</label><br>
		<label>
			<input type="radio" name="q2" value="c">
			c) Факультет стал презентабельным
		</label><br><br>

		<h2>Вопрос 3:</h2>
		<p>Кто вам дороже: мама или Кристина?</p>
		<label>
			<input type="radio" name="q3" value="a">
			a) Пздц у вас тут вопросы...
		</label><br>
		<label>
			<input type="radio" name="q3" value="b">
			b) Кристина
		</label><br>
		<label>
			<input type="radio" name="q3" value="c">
			c) Мама
		</label><br><br>

		<input type="submit" value="Закончить тест и узнать результат (скрины в беседу)">
	</form>
	
	<div id="quiz-results" style="display:none;">
		<h2>Результат:</h2>
		<p>Поздравляю!!! Вы набрали <span id="num-correct"></span> из 3 правильных вопросов. А теперь можно идти на пары,зная о Кристинке всё.</p>
	</div>

	<script>
		document.getElementById("quiz-form").addEventListener("submit", function(event) {
			event.preventDefault();
			let numCorrect = 0;
			if (document.querySelector('input[name="q1"]:checked').value === "b") {
				numCorrect++;
			}
			if (document.querySelector('input[name="q2"]:checked').value === "b") {
				numCorrect++;
			}
			if (document.querySelector('input[name="q3"]:checked').value === "c") {
				numCorrect++;
			}
			document.getElementById("num-correct").innerHTML = numCorrect;
			document.getElementById("quiz-form").style.display = "none";
			document.getElementById("quiz-results").style.display = "block";
		});
	</script>
</body>
</html>
