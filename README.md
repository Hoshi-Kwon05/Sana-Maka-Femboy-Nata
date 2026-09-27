<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Hart's Birthday 🎂</title>

<style>

/* =========================
   BASIC SETUP
========================= */

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100vh;
    font-family: Arial, sans-serif;
    background: #fff;
    color: #625b65;
    overflow-x: hidden;
}

/* SOFT BACKGROUND */

body::before {
    content: "";
    position: fixed;
    width: 280px;
    height: 280px;
    border-radius: 50%;
    background: #fff0f6;
    top: -140px;
    left: -140px;
    z-index: -1;
}

body::after {
    content: "";
    position: fixed;
    width: 280px;
    height: 280px;
    border-radius: 50%;
    background: #f0edff;
    right: -140px;
    bottom: -140px;
    z-index: -1;
}

/* =========================
   FLOATING DECOR
========================= */

.float {
    position: fixed;
    z-index: 20;
    cursor: pointer;
    color: #d69ab6;
    animation: float 4s ease-in-out infinite;
}

.f1 {
    top: 12%;
    left: 7%;
    font-size: 25px;
}

.f2 {
    top: 28%;
    right: 8%;
    font-size: 20px;
    animation-delay: 1s;
}

.f3 {
    bottom: 20%;
    left: 9%;
    font-size: 22px;
    animation-delay: 2s;
}

.f4 {
    bottom: 12%;
    right: 8%;
    font-size: 27px;
    animation-delay: 1.5s;
}

@keyframes float {

    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-12px);
    }
}

/* =========================
   CONTAINER
========================= */

.container {
    width: min(92%, 560px);
    margin: auto;
    padding: 28px 0 60px;
}

/* =========================
   TOP PROGRESS
========================= */

.top {
    display: flex;
    justify-content: space-between;
    color: #aaa;
    font-size: 12px;
    margin-bottom: 10px;
}

.progress {
    height: 5px;
    background: #eee8ee;
    border-radius: 20px;
    overflow: hidden;
    margin-bottom: 25px;
}

.progress-fill {
    height: 100%;
    width: 14%;
    background: #d596b3;
    transition: .5s;
}

/* =========================
   PAGES
========================= */

.page {
    display: none;
}

.page.active {
    display: block;
    animation: appear .4s ease;
}

@keyframes appear {

    from {
        opacity: 0;
        transform: translateY(15px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* =========================
   CARD
========================= */

.card {
    background: rgba(255,255,255,.98);
    border: 1px solid #eee8ee;
    border-radius: 28px;
    padding: 38px 25px;
    text-align: center;
    box-shadow: 0 12px 35px rgba(80,60,80,.08);
}

.emoji {
    font-size: 55px;
    margin-bottom: 15px;
    animation: bounce 2s infinite;
}

@keyframes bounce {

    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-8px);
    }
}

h1 {
    color: #d28da9;
    font-size: clamp(34px, 9vw, 48px);
    margin-bottom: 15px;
}

h2 {
    color: #8975b3;
    font-size: clamp(24px, 7vw, 34px);
    margin-bottom: 15px;
}

p {
    line-height: 1.7;
    margin-bottom: 18px;
}

/* =========================
   BUTTONS
========================= */

button {
    border: none;
    border-radius: 50px;
    padding: 14px 23px;
    min-height: 48px;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    transition: .25s;
}

button:hover {
    transform: translateY(-3px);
}

button:active {
    transform: scale(.95);
}

.primary {
    background: #d596b3;
    color: white;
}

.purple {
    background: #9583bf;
    color: white;
}

.light {
    background: #faf8fb;
    color: #786b80;
    border: 1px solid #e3dbe5;
}

/* =========================
   NO BUTTON
========================= */

#noButton {
    position: relative;
}

/* =========================
   QUIZ / RESULTS
========================= */

.quiz-options {
    display: grid;
    gap: 12px;
    margin: 20px 0;
}

.quiz-option {
    border: 1px solid #e4dce6;
    border-radius: 18px;
    padding: 16px;
    cursor: pointer;
    transition: .25s;
    background: white;
    color: #625b65;
}

.quiz-option:hover {
    background: #fff5f8;
    transform: translateY(-2px);
}

.quiz-result {
    min-height: 30px;
    color: #d28da9;
    font-weight: bold;
}

/* =========================
   DATE PICKER
========================= */

.date-box {
    margin: 25px 0;
}

#birthdayDate {
    width: 100%;
    padding: 16px;
    border-radius: 18px;
    border: 1px solid #e4dce6;
    background: #fffafd;
    color: #625b65;
    font-size: 16px;
    text-align: center;
    outline: none;
    cursor: pointer;
}

#birthdayDate:focus {
    border-color: #d596b3;
    box-shadow: 0 0 0 3px #fff0f6;
}

/* =========================
   GIFTS
========================= */

.gifts {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin: 25px 0;
}

.gift {
    font-size: 55px;
  setTimeout(function() {
            nextPage(7);
        }, 2800);
    } else {
        result.textContent = "jema ka dae, ang pinaka daghan pilia. 😭";
    }
}

function balloonExplosion() {
    const balloons = [
        "🎈","🎈","🎈","🎈","🎈",
        "🎈","🎈","🎈","🎈","🎈",
        "🎈","🎈","🎈","🎈","🎈",
        "🎈","🎈","🎈","🎈","🎈"
    ];

    balloons.forEach(function(balloon, index) {
        setTimeout(function() {
            const element = document.createElement("div");

            element.className = "balloon-confetti";
            element.textContent = balloon;

            element.style.left = Math.random() * 100 + "%";

            element.style.setProperty(
                "--side",
                (Math.random() * 300 - 150) + "px"
            );

            element.style.setProperty(
                "--rotate",
                (Math.random() * 360 - 180) + "deg"
            );

            element.style.fontSize =
                (28 + Math.random() * 28) + "px";

            document.body.appendChild(element);

            setTimeout(function() {
                element.remove();
            }, 3200);

        }, index * 70);
    });
}


/* =========================
   HEART BURST
========================= */

function heartBurst() {

    for (let i = 0; i < 14; i++) {

        const heart =
            document.createElement("div");

        heart.className = "heart";

        heart.textContent =
            ["♡", "♥", "✦", "✧"][
                Math.floor(
                    Math.random() * 4
                )
            ];

        heart.style.left = "50%";
        heart.style.top = "50%";

        document.body.appendChild(
            heart
        );

        setTimeout(function() {

            const x =
                (Math.random() - 0.5) * 320;

            const y =
                (Math.random() - 0.5) * 320;

            heart.style.transform =
                "translate(" +
                x +
                "px," +
                y +
                "px)";

            heart.style.opacity = "0";

        }, 30);

        setTimeout(function() {

            heart.remove();

        }, 1100);
    }
}


/* =========================
   STAR-ONLY CONFETTI
========================= */

function createConfetti() {

    const symbols = [
        "★",
        "☆",
        "✦",
        "✧",
        "⋆",
        "✩"
    ];

    const colors = [
        "#d596b3",
        "#a99bd0",
        "#e3ca75",
        "#a9c9e5"
    ];

    for (let i = 0; i < 70; i++) {

        const piece =
            document.createElement(
                "div"
            );

        piece.className =
            "confetti";

        piece.textContent =
            symbols[
                Math.floor(
                    Math.random() *
                    symbols.length
                )
            ];

        piece.style.left =
            Math.random() * 100 +
            "vw";

        piece.style.color =
            colors[
                Math.floor(
                    Math.random() *
                    colors.length
                )
            ];

        piece.style.fontSize =
            (10 + Math.random() * 18) +
            "px";

        piece.style.animationDuration =
            (2 + Math.random() * 3) +
            "s";

        document.body.appendChild(
            piece
        );

        setTimeout(function() {

            piece.remove();

        }, 5500);
    }
}


/* =========================
   FINAL CHAOS
========================= */

function finalChaos() {

    createConfetti();

    heartBurst();

    setTimeout(
        createConfetti,
        500
    );

    setTimeout(
        heartBurst,
        800
    );

    setTimeout(
        createConfetti,
        1200
    );

    setTimeout(
        heartBurst,
        1500
    );

    document.getElementById(
        "final"
    ).innerHTML = `

        <div class="final-box">

            🎉 OFFICIAL RESULT 🎉

            <br><br>

            Hart has successfully survived
            another year.

            <br><br>

            A diva
    An Icon
   
  
          
            

            <br><br>

            HAPPY BIRTHDAY, HARTTT!

        </div>

    `;
}


/* =========================
   START
========================= */

nextPage(1);

</script>

</body>
</html>
