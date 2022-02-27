# regular-expressions

in php how can we set regex for date

<?php

$string = '10/01/2021';

$ans1 = preg_match('~(0[1-9]|1[012])[-/.](0[1-9]|[12][0-9]|3[01])[-/.](19|20)\d\d~',$string);
if($ans1==1){
	echo "Pattern Match " . $string;
}
else{
	echo "Pattern does not Match " . $string;
}


?>

# Hexa-Decimal Validation

<?php

$errorMessage = "";
$pattern = "/^(0x|0X)?[a-fA-F0-9]+$/";
$userInput = "";
$isMatch = false;


if ($_SERVER['REQUEST_METHOD'] == "POST") {

    if (!empty($_POST['userInput'] && strlen($_POST['userInput']) == 2)) {
        $userInput = $_POST['userInput'];
        if (preg_match($pattern, $_POST['userInput'], $matches) == 0) {            
            $errorMessage = "'{$userInput}' is not a valid hexadecimal number";
        }else{
            $isMatch = true;
        }
    } else {
        $errorMessage = "User input must be only 2 characters long";
    }
}

?>
