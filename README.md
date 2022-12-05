# Moving 2D Scene
It is a project that uses java script to create a 2D scene that mas moving objects on the canvas. This project uses javascript and html. It is set out in the subroutine hierarchy formate. It create objects that move by translation, rotation and scale.

## Idea

Create the character Sonic the Hedgehog in Green Hills. It has the sun flowers that rotate and waves that move. The character runs across the screen.

## How the code works
Draw shape:
```diff
var shoeOutln = new SceneGraphNode();
	shoeOutln.doDraw = function(g){
		g.beginPath();
		g.moveTo(0, 0);
		g.bezierCurveTo(0,0.6, 0.8,0.5, 1.30,0);
		g.stroke();
		g.closePath();
		g.fill();
	}
```

rotate object per frame:
```diff
 leaf.setRotation(Math.sin(frameNumber/20)*6);
```
create a new object and set scale, rotation and tranlation :

```diff
var tri = new TransformedObject(filledTriangle).setScale(0.3,0.3).setTranslation(0,0.19).setColor("yellow"); // for sunflower petal
		var templeaf = new CompoundObject();
		templeaf.add(new TransformedObject(filledRect).setScale(0.2,0.2).setRotation(45).setColor("green"));
		templeaf.add(new TransformedObject(filledTriangle).setScale(0.3,0.15).setColor("#72d74e"));
		leaf =  new TransformedObject(templeaf);
```
