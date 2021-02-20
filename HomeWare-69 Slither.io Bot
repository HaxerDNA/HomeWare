// ==UserScript==
// @name         Homeware SlitherIO Bot
// @namespace    Homeware SlitherIO Bot
// @version      0.0.1
// @description  This is a bot for Slither.io, created by Homeware.
// @author       Homeware
// @homepage     coming soon...
// @iconURL       https://cdn.discordapp.com/attachments/812250948716986398/812773442545516544/HomewarePFP.jpg
// @match         http://slither.io/
// @supportURL    https://discord.gg/bngY3TryZX
// @include       https://code.jquery.com/jquery-3.5.1.min.js
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
var options = {
    bot: false
};
console.log(`
 ▄▄▄▄    ▒█████  ▄▄▄█████▓
▓█████▄ ▒██▒  ██▒▓  ██▒ ▓▒
▒██▒ ▄██▒██░  ██▒▒ ▓██░ ▒░
▒██░█▀  ▒██   ██░░ ▓██▓ ░
░▓█  ▀█▓░ ████▓▒░  ▒██▒ ░
░▒▓███▀▒░ ▒░▒░▒░   ▒ ░░
▒░▒   ░   ░ ▒ ▒░     ░
 ░    ░ ░ ░ ░ ▒    ░
 ░          ░ ░
      ░

by
██╗  ██╗ ██████╗ ███╗   ███╗███████╗
██║  ██║██╔═══██╗████╗ ████║██╔════╝
███████║██║   ██║██╔████╔██║█████╗
██╔══██║██║   ██║██║╚██╔╝██║██╔══╝
██║  ██║╚██████╔╝██║ ╚═╝ ██║███████╗
╚═╝  ╚═╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝

██╗    ██╗ █████╗ ██████╗ ███████╗
██║    ██║██╔══██╗██╔══██╗██╔════╝
██║ █╗ ██║███████║██████╔╝█████╗
██║███╗██║██╔══██║██╔══██╗██╔══╝
╚███╔███╔╝██║  ██║██║  ██║███████╗
 ╚══╝╚══╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝
`);

function moveTo(x, y) {
    xm = x - snake.xx;
    ym = y - snake.yy;
}

function ui() {
    tips();
    document.getElementsByTagName('head')[0].appendChild(link);
}

function tips() {
    document.getElementById("tips").innerHTML = "Version: 1.0.0 by Homeware";
}

var nearestFood = foods[0];

function moveTo2() {
    if (options.bot) {
        moveTo(nearestFood.xx, nearestFood.yy);
    }
}

function getDistance(point1, point2) {
    return Math.sqrt(Math.pow(point1.xx - point2.xx, 2) + Math.pow(point1.yy - point2.yy, 2));
}

function goEat() {
    if (options.bot) {
        var shortestDistance = 999999999;
        var distance = 0;
        var iter = 0;
        for (iter; iter < foods.length-1; iter++) {
            if (foods[iter] == null) continue;
            distance = getDistance(foods[iter], snake);
            if (distance < shortestDistance) {
                shortestDistance = distance;
                nearestFood = foods[iter];
            }
        }
    }
}

function stuck() {
    nearestFood = foods[0];
}

var names = ["(Sli)<the>[r]{IO}", "Loooooonnnnnggggg", "Maximus", "Sun#", "Moon#", "W3B#", "4ZUR3Fan#", "NoKiddy#", "Titus Vibius#", "Caesar#", "Caius Considius#"];

document.getElementById("twth").style.visibility = "hidden";
document.getElementById("fbh").style.visibility = "hidden";
document.getElementById("grqh").style.visibility = "hidden";
document.getElementById("clq").style.visibility = "hidden";
var logo = document.getElementById("logo");
logo.innerHTML = "<div style=\"width: 450px; height: 115px;\"><h1 style=\"font-family: Arial, Helvetica, sans-serif;color: #ffffff;font-size: 125px;\" id=\"voidlogo\">V01D</h1></div>";

var play = document.getElementById("playh");
var active = document.createElement("P");
active.innerHTML = "<lable style=\"text-align: left;color: #ffffff;font-family: Arial, Helvetica, sans-serif;\">[r] Bot: </lable><label id=\"botstatus\" style=\"color: #cc0000;font-family: Arial, Helvetica, sans-serif;\">false</label>"
play.appendChild(active);

document.getElementById("nick").value = names[Math.floor((Math.random() * names.length))] + Math.floor((Math.random() * 10000) + 0);
document.title = "[r] Homeware Bot";
var link = document.querySelector("link[rel*='icon']") || document.createElement('link');
link.type = 'image/x-icon';
link.rel = 'shortcut icon';
link.href = 'https://cdn.discordapp.com/attachments/812250948716986398/812252125345742848/iconfinder-snake-4591880_122131.png';

document.addEventListener('keyup', (e) => {
    const key = event.key.toLowerCase();
    var enabled = document.getElementById("botstatus");
    if (key === "r") {
        if (options.bot) {
            options.bot = false;
            enabled.innerHTML = "false";
            enabled.style.color = "#cc0000";
            document.title = "[r] Homeware inactive";
            var link = document.querySelector("link[rel*='icon']") || document.createElement('link');
            link.type = 'image/x-icon';
            link.rel = 'shortcut icon';
            link.href = 'https://cdn.discordapp.com/attachments/812250948716986398/812252125345742848/iconfinder-snake-4591880_122131.png';
        } else {
            options.bot = true;
            enabled.innerHTML = "true";
            enabled.style.color = "#00cc00";
            document.title = "[r] Homeware active";
            var link = document.querySelector("link[rel*='icon']") || document.createElement('link');
            link.type = 'image/x-icon';
            link.rel = 'shortcut icon';
            link.href = 'https://cdn.discordapp.com/attachments/812250948716986398/812770915279568986/circle-cropped.png';
        }
    }
});

goEat();
setInterval(moveTo2, 20);
setInterval(goEat, 300);
setInterval(stuck, 1000);
setInterval(ui, 150);
})();
