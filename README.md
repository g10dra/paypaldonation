# paypaldonation
paypal donation form

Hello All,
                 I am sharing a very simple  code snippet  for making a donation form where admin can get receive donation from internet via paypal payment gateway



<script>
function validation()
{

  var amount1=document.getElementById("amount1").value;
 
  var amount2=document.getElementById("amount2").value;

if(amount1 > 0)
{

}
else
{
 
  document.getElementById("amount1").value="10"; 

}
if(amount2 > 0)
{

}
else
{
 
  document.getElementById("amount2").value="10"; 

}
document.getElementById("business").value="jeetu91.singh@gmail.com";
document.getElementById("item_name").value="Donation to jeetendra singh";
document.getElementById("currency_code").value="USD";

return true;
}
</script>

<form name="_xclick" style="background-color:silver;border:1px solid red;width:300px" action="https://www.paypal.com/cgi-bin/webscr" onsubmit="return validation()" method="post">
<h3>Make a Small Donation To Me</h3>
<input type="hidden" name="cmd" value="_xclick">
<input type="hidden" id="business" name="business" value="jeetu91.singh@gmail.com">
<!--change the value of business as your paypal email account-->
<input type="hidden" name="item_name" id="item_name" value="Donation to jeetendra singh">
<input type="hidden" name="currency_code" id="currency_code" value="USD">
<p><input name="choose" checked="checked" type="radio" onclick="document.getElementById('amount2').disabled=true;document.getElementById('amount1').disabled=false" />Choose Amount <input name="choose" type="radio" onclick="document.getElementById('amount1').disabled=true;document.getElementById('amount2').disabled=false" />Custom Amount</p><p>
Choose Amount:<select style="width:180px;" id="amount1" name="amount">
 <option selected="selected" value="10">will take a drink in $10.00 USD</option>
 <option value="20">will be fun with friends in $20.00 USD</option>
 <option value="50">will go cinema with my wife in $50.00 USD</option>
 <option value="100">will be getting dinner in 5 star with my wife in $100.00 USD</option>
</select></p> <p>
Custom Amount:<input type="text" disabled="disabled" name="amount" id="amount2" value="15" />
</p><p>
<input type="image" src="https://www.paypal.com/en_US/i/btn/btn_donate_LG.gif" border="0" name="submit" alt="Make a donation with PayPal">
</p>
</form>

