---
layout: 	post
title: 		Cause of Death
date: 		2017-11-05 06:56:24 -0800
categories: programming
---

Being very bored, I asked my friends on instagram for program ideas. One of them was a generator causes of death, so here it is. Rather than randomly outputting from an array, this takes the probability of the leading causes into account.

Source: [https://www.cdc.gov/nchs/data/hus/hus16.pdf#017](https://www.cdc.gov/nchs/data/hus/hus16.pdf#017)


<p id="cause"></p> <button onclick="update()">Die!</button>


Here is the code!

``` javascript
function update() {
	document.getElementById("cause").innerHTML = cod()
}
	
function cod() {
	let p = Math.random() * 733.1

	console.log(p)

	switch (true) {
	case p < 168.5: return "Heart disease"
	case p < 327: return "Cancer"
	case p < 368.6: return "Chronic lower respiratory disease"
	case p < 411.8: return "Unintentional injuries"
	case p < 449.4: return "Stroke"
	case p < 478.8: return "Alzheimer's disease"
	case p < 500.1: return "Diabetes"
	case p < 515.3: return "Influenza and pneumonia"
	case p < 528.7: return "Nephritis, nephrotic syndrome, or nephrosis"
	case p < 542: return "Suicide"
	default: return randomDisease()
	}
}

var diseaseArr = [
	"Overdose", "Lightning", "Car accident",
	"Homicide", "Genocide", "Food poisoning",
	"Global thermonuclear war", "Aliens",
	"Mentally ill and sad white man",
	"Uncivilized and dangerous black man",
]

function randomDisease() {
	i = Math.floor(Math.random() * diseaseArr.length)

	return diseaseArr[i]
}
```

<script type="text/javascript">

function update() {
	document.getElementById("cause").innerHTML = cod()
}
	
function cod() {
	let p = Math.random() * 733.1

	console.log(p)

	switch (true) {
	case p < 168.5: return "Heart disease"
	case p < 327: return "Cancer"
	case p < 368.6: return "Chronic lower respiratory disease"
	case p < 411.8: return "Unintentional injuries"
	case p < 449.4: return "Stroke"
	case p < 478.8: return "Alzheimer's disease"
	case p < 500.1: return "Diabetes"
	case p < 515.3: return "Influenza and pneumonia"
	case p < 528.7: return "Nephritis, nephrotic syndrome, or nephrosis"
	case p < 542: return "suicide"
	default: return randomDisease()
	}
}

var diseaseArr = [
	"Overdose", "Lightning", "Car accident",
	"Homicide", "Genocide", "Food poisoning",
	"Global thermonuclear war", "Aliens",
	"Mentally ill and sad white man",
	"Uncivilized and dangerous black man",
]

function randomDisease() {
	i = Math.floor(Math.random() * diseaseArr.length)

	return diseaseArr[i]
}

</script>