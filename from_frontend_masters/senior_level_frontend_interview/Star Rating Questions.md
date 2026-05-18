**What is difference between controlled and uncontrolled elements?**
	Controlled: Parent manages state via value + onChange
	< StarRating value={rating} onChange={setRating} />
	Uncontrolled: Component manages its own state via defaultValue
	< StarRating defaultValue={3} />
	
**What does it mean by Accessible in web development**
	Accessible means your website works for **everyone** — including people who:
	- can't use a mouse (use keyboard only)
	- are blind (use screen readers that read the page out loud)
	- have motor disabilities (use voice control)
	
**What does it mean by "use closest accessible element"**
	This means — pick the HTML element whose **built-in behavior already matches** what you're building.

**What is the "dataset" target.dataset in javascript?**
	It allows to get data attribute from the html element.