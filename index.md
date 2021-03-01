## Who merges?
<div id="text"></div>
<script>
var week = ISO8601_week_no(new Date());
var mergerNum = week % 9;
var merger;
switch (mergerNum) {
  case 0: 
    merger = 'Mikal'
    break;
  case 1:
    merger = 'Per-Olav'
    break;
  case 2:
    merger = 'Erlend'
    break;
  case 3:
    merger = 'Øyvind'
    break;
  case 4:
    merger = 'Anders'
    break;
  case 5:
    merger = 'Thomas'
    break;
  case 6:
    merger = 'Eivind'
    break;
  case 7:
    merger = 'Morten'
    break;
  case 8:
    merger = 'Sachin'
    break;
  
  }
document.getElementById("text").innerHTML = 'week is: ' + merger;

function ISO8601_week_no(dt) 
  {
     var tdt = new Date(dt.valueOf());
     var dayn = (dt.getDay() + 6) % 7;
     tdt.setDate(tdt.getDate() - dayn + 3);
     var firstThursday = tdt.valueOf();
     tdt.setMonth(0, 1);
     if (tdt.getDay() !== 4) 
       {
      tdt.setMonth(0, 1 + ((4 - tdt.getDay()) + 7) % 7);
        }
     return 1 + Math.ceil((firstThursday - tdt) / 604800000);
        }
</script>
