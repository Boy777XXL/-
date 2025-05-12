# -<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8">
  <title>СІРИЙ КОШЕЛЬ</title>
  <style>
    body {
      background-color: #983112;
      color: white;
      font-family: 'Arial Black', sans-serif;
      text-align: center;
      padding: 20px;
    }
    .button {
      background-color: black;
      color: white;
      padding: 10px 20px;
      border: none;
      font-size: 18px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <audio autoplay loop>
    <source src="https://zvukogram.com/zvuk/79247/" type="audio/mpeg">
    Ваш браузер не підтримує елемент <code>audio</code>.
  </audio>

  <img src="file:///D:/Users/First/Desktop/%D0%BA%D0%BE%D1%88%D0%B5%D0%BB%D0%B5%D0%BA.png" alt="Сірий Кошель" width="300"><br><br>

  <img src="file:///D:/Users/First/Desktop/%D0%B1%D0%B0%D0%BD%D0%BD%D0%B5%D1%80.png" alt="Поп-Арт Банер" width="100%"><br><br>

  <h2>СІРИЙ ID</h2>
  <p>Зареєструй свій гаманець у найнадійнішій системі обліку легенд.</p>
  <form onsubmit="registerID(); return false;">
    <label for="name">Ім'я:</label><br>
    <input type="text" id="name" name="name" required><br><br>
    <label for="surname">Прізвище:</label><br>
    <input type="text" id="surname" name="surname" required><br><br>
    <button type="submit" class="button">Зареєструвати гаманець</button>
  </form>
  <p id="idResult" style="margin-top: 20px; font-size: 18px;"></p>

  <div id="greyLevel" style="margin-top: 30px;">
    <h3>Рівень Сірості</h3>
    <div style="background: #ddd; width: 100%; height: 25px; border-radius: 10px; overflow: hidden;">
      <div id="greyBar" style="background: grey; width: 0%; height: 100%; transition: width 1s;"></div>
    </div>
    <p id="greyText" style="font-weight: bold; margin-top: 10px;"></p>
  </div>

  <h2>БІРЖА СІРОСТІ</h2>
  <p>₴ Груша / UAH — 134.00</p>
  <p>₴ Квасоля / UAH — 88.10</p>
  <p>₴ Ананас / UAH — 1 122.22</p>

  <script>
    function registerID() {
      const name = document.getElementById('name').value;
      const surname = document.getElementById('surname').value;
      const phrases = [
        "Вас внесено до Реєстру Сірого Народу!",
        "Гаманець активовано. Вінниччина пишається вами.",
        "Тепер ви — повноправний носій Сірого Кошеля.",
        "Ваші буряки будуть у безпеці.",
        "Ананас посвятив ваше ім’я у фінансову легенду."
      ];
      const message = phrases[Math.floor(Math.random() * phrases.length)];
      document.getElementById('idResult').innerHTML = `<strong>${name} ${surname}:</strong> ${message}`;
      showGreyLevel();
    }

    function showGreyLevel() {
      const level = Math.floor(Math.random() * 101);
      document.getElementById('greyBar').style.width = level + '%';
      document.getElementById('greyText').innerText = 'Ваш рівень сірості: ' + level + '%';
    }
  </script>
</body>
</html>
