# Ventti
<!DOCTYPE html>

<html>

<head>
	<meta charset="utf-8" />
	<head><title>Ventti</title>

<h1>Ventti</h1>

<p id="Pelaajan kortit"></p>
<p id="Tietokoneen kortit"></p>
<p id="message"></p>



<button onclick="Pelaa()">Pelaa</button>

<script>
function Pelaa() {
    var num1, num2,num3, num4, sum1, sum2, pelaaja, tietokone;
	
    num1 = Math.floor(Math.random()*13) + 1;
    num2 = Math.floor(Math.random()*13) + 1;
    num3 = Math.floor(Math.random()*13) + 1;
	num4 = Math.floor(Math.random()*13) + 1;
    sum1 = num1 + num2;
	sum2 = num3 + num4;
    pelaaja = num1 + num2;
	tietokone = num3 + num4;
	document.getElementById("Pelaajan kortit").innerHTML = "Pelaajan kortit: " + num1 + " + " + num2 + " = " +sum1;
	document.getElementById("Tietokoneen kortit").innerHTML = "Tietokoneen kortit: " + num3 + " + " + num4 + " = " +sum2;
	
	
	
	if (sum1 > 21 && sum2 >21) {
		document.getElementById("message").innerHTML = "Tasuri!";
	}
	else if (sum1 == sum2) {
		document.getElementById("message").innerHTML = "Tasapeli!";
	}
	else if (sum1 >= 22) {
		document.getElementById("message").innerHTML = "Tietokone voitti!"
	}
	else if (sum2 >= 22) {
		document.getElementById("message").innerHTML = "Pelaaja voitti!"
	}
	else if (sum1 > sum2) {
		document.getElementById("message").innerHTML = "Pelaaja voitti!";
	}
	else if (sum2 > sum1) {
		document.getElementById("message").innerHTML = "Tietskari voitti!";
	}
	
	
}


</script>
</head>




</body>
</html>
