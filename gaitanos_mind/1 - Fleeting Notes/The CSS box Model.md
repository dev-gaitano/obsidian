What is the box model?
What does it do?
Why is it important?

All elements in CSS are a box either rectangular or square.

Content - The element
	Padding - add background to an element.
		Border - add a border around the element
			Margin - space two elements apart from each other

```
* {
    padding: 0;
    margin: 0;
    font-size: 40px;
}

.box-one {
    background-color: #EB5757;
    padding: 10px;
    height: 100px;
    width: 100px;
    border: 30px solid #9B51E0;
    margin: 60px;
}

.box-two {
    background-color: #2D9CDB;
    border: 0 solid #27AE60;
}

```

Cementic HTML