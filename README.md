# type-checkbox-using-php-GET
none, one or multiple inputs returned using php

<form action="submitpage3.php">
<?php 
if ((!isset($_GET["items"]))||(empty($_GET["itemss"]))){
	if ((isset($_GET["items"]))&&(empty($_GET["items"]))){
		$error="No items entered.";	}
?>
<p>What items did you order?<br>
<input id="CBBigMick"   type="checkbox" name="items[]" value="Big Mick"            /><label for="CBBigMick">Big Mick Burger</label>
<input id="CBMcChick"   type="checkbox" name="items[]" value="McChick Sandwich"    /><label for="CBMcChick">McChick Sandwich</label><br>
<input id="CBMcDog"     type="checkbox" name="items[]" value="McDog"               /><label for="CBMcDog">McDog</label>
<input id="CBFries"     type="checkbox" name="items[]" value="Galaxy Famous Fries" /><label for="CBFries">Galaxy Famous Fries</label><br>
<input id="CBRings"     type="checkbox" name="items[]" value="McRings"             /><label for="CBRings">McRings</label>
<input id="CBShakes"    type="checkbox" name="items[]" value="McShakes"            /><label for="CBShakes">McShakes</label>
</p>							 
<input type="submit" name="submit" value="Next" />
</form>
<?php
}
?>
<?php
}else{
?>
<?php
    if (!isset($_GET["items"])){
	 echo "<p>You chose the following items: none selected.</p>";
}else{
	 echo "<p>You chose the following items: ".implode(", ",$_GET['items'])."</p>";
}
?>	
<a href="submitpage4.php">
<input type="button" value="Next" />
</a>
<?php
}
?>
