## Who merges?


<div id="text"></div>
<script>
var onejan = new Date(this.getFullYear(),0,1);
var millisecsInDay = 86400000;
var weekNum = Math.ceil((((this - onejan) /millisecsInDay) + onejan.getDay()+1)/7);
document.getElementById("text").innerHTML = "week is: "+weekNum;
</script>
