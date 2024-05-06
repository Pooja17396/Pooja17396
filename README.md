<!DOCTYPE html>   
<head>   
<title> Using fucntions    
</title>   
</head>   
<?php   
$Number_no_1 = $_POST['Number_no_1ber'];   
$Number_no_2 = $_POST['Number_no_2ber'];   
$Result = $_POST['Result'];   
function MyCalculator($Number1,$Number2, $Result)    
// set $Result as parameter   
{   
switch($Result)   
{   
case "Addition":    
// here you have to use colons not semi-colons   
$compute = $Number1 + $Number2;    
break;   
case "Subtraction":   
$compute = $Number1 - $Number2;    
break;   
case "Multiplication":   
$compute = $Number1 * $Number2;    
break;   
case "Division":   
$compute = $Number1 / $Number2;    
break;   
}   
return $compute; // returning variable   
}   
echo "$Result <br /> <br /> 1st Number: $Number_no_1 <br /> 2nd Number: $Number_no_2 <br /><br />";   
echo "Answer is:" .MyCalculator($Number_no_1,$Number_no_2, $Result);   
// you need to pass $Result as argument of that function   
?>   
<body>   
<div id="page-wrap">   
<h1>Calculator by Nirnay</h1>   
<form action="" method="post" id="quiz-form">   
<p>   
<input type="number" name="Number_no_1" id="Number_no_1" required="required" value="<?php echo $Number_no_1; ?>" /> <b>First Number</b>   
</p>   
<p>   
<input type="number" name="Number_no_2" id="Number_no_2" required="required" value="<?php echo $Number_no_2; ?>" /> <b>Second Number</b>   
</p>   
<p>   
<input readonly="readonly" name="CalculatorResult" value="<?php echo $CalculatorResult; ?>"> <b>CalculatorResult</b>   
</p>   
<input type="submit" name="operator_specified" value="Sum" />   
<input type="submit" name="operator_specified" value="Subtraction" />   
<input type="submit" name="operator_specified" value="Multiplication" />   
<input type="submit" name="operator_specified" value="Division" />   
</form>   
</div>   
</body>   
</html>   
