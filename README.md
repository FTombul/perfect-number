perfect-number
==============

perfect number


var maxVollkommenZahl = 10000;
var divIdVollkommeneZahlen = 'vollkommeneZahlen';

function berechneVollkommeneZahlen() {
	var vollkommeneZahl = 2;
	var teiler = 1;
	var summeTeiler = 0;
	
	for (vollkommeneZahl = 2; vollkommeneZahl <= maxVollkommenZahl; ++vollkommeneZahl) {
		summeTeiler = 0;
		for(teiler = 1; teiler < (vollkommeneZahl / 2 +1); ++teiler) {
			if((vollkommeneZahl % teiler) == 0) {
				summeTeiler += teiler;
			}
		}
		
		if (summeTeiler == vollkommeneZahl) {
			document.getElementById(divIdVollkommeneZahlen).innerHTML += vollkommeneZahl + '<br />';
		}
	}
}
