## Who merges?


<div id="text"></div>
<script>

document.getElementById("text").innerHTML = 'week is: ' + nextweek();

function nextweek(){
    var today = new Date();
    var nextweek = new Date(today.getFullYear(), today.getMonth(), today.getDate()+7);
    return nextweek;
}
</script>
