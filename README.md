# PHP-practical-program-3


<!DOCTYPE html>
<html>
<body>

<form method="post">
Units:
<input type="number" name="units">
<input type="submit" name="submit" value="Calculate">
</form>

<?php
if(isset($_POST['submit']))
{
    $units = $_POST['units'];

    if($units <= 100)
        $bill = $units * 2;
    elseif($units <= 200)
        $bill = 200 + ($units - 100) * 3;
    else
        $bill = 500 + ($units - 200) * 5;

    echo "Total Bill = Rs. " . $bill;
}
?>

</body>
</html>


Output
For input 150 units:
Units: 150
[Calculate]

Total Bill = Rs. 350
