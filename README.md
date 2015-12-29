#Design Concept

0. A collection of common chart based on d3.js
1. Following Mike Bostock's [Reusable Chart](http://bost.ocks.org/mike/chart/) pattern
2. Responsive using SVG viewbox
3. Entering Animation
4. Flexible (the following clock is built using settimeinterval with donut chart)

![clock](/doc/demo.gif)




#Example Bar Chart

[See it in action](http://iing.tw/policies/long-term_care)


		data = [
			{"key": '彰化碧峰里', "value": 	43}
			{"key": '花蓮森榮里', "value": 	41}
			{"key": '南投光明里', "value": 	41}
			{"key": '台灣平均', "value": 	12}
			{"key": '新竹東平里', "value": 	2}
			{"key": '新竹關新里', "value": 2}
			{"key": '新竹大鵬里', "value": 2}
		]

		firstBar = barChart!
			.data data
			.container '#bar' ### the container where to init the bar chart
			.barHeight 25


		firstBar! ### call this when page init, so that the svg is being initiated, and the space is saved


		firstBar.draw! ### when user actually scroll to the viewport, then start entering animation