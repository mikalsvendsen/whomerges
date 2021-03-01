## Who merges?


<div id="text"></div>
<script>

document.getElementById("text").innerHTML = 'week is: ' + week();

function week(){
    var today = new Date();
    return today.getWeek();
}

Date.prototype.getWeek = function () {
    var onejan = new Date(this.getFullYear(), 0, 1);
    return Math.ceil((((this - onejan) / 86400000) + onejan.getDay() + 1) / 7);
};
</script>
