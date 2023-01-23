<style>
div{margin: 10px;padding: 5px;}
</style>
<script>
function getamt()
{
debugger;
var s=document.getElementById("source");
var sr=s.options[s.selectedIndex].text;
var d=document.getElementById("des");
var ds=d.options[d.selectedIndex].text;
if(sr==ds)
{
alert("Source City & Desination City Same!!!");
}
else
{
var dsv=d.options[d.selectedIndex].value;
var ns=document.getElementById("txtSeat").value;
var tm=parseInt(ns)*parseInt(dsv);
document.getElementById("txtAmt").value=tm;
}
}
</script>
</head>
<body>
<form>
<div>
<label>Select Source City</label>
<select id="source">
<option>--Select--</option>
<option>Mysuru</option>
<option>Bangalore</option>
<option>Kerala</option>
</select>
</div>
<div>
<label>Select Desination City</label>
<select id="des">
<option>--Select--</option>
<option value="150">Mysuru</option>
<option value="150">Bangalore</option>
<option value="250">Kerala</option>
</select>
</div>
<div>
<label>Enter No of Seats</label>
<input type="number" id="txtSeat" />
</div>
<div>
<label>Total Amount</label>
<input type="text" id="txtAmt" readonly />
</div>
<div>
<input type="button" value="Get Amount" onclick="getamt()"/>
</div>
</form>
</body>
</html>
