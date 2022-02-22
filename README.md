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
