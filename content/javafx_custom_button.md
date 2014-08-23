Title: JavaFX custom button
Date: 2009-7-5 7:35
Category: Tech
Tags: tech, programming, javafx
Slug: javafx-custom-button
Author: Vaibhav Mishra
Summary: JavaFX custom button.


<div dir="ltr" style="text-align: left;" trbidi="on">
I am creating a simple application just to learn intricacies of javafx, the application require a button component, I know it is quite easy to use swing button , but it is just plain ugly and do not belnd with my application UI, nothing special , I just wanted a simple application so I created a simple button component were<br />
<ol>
<li>A simple rectangle which forms the button surrounding</li>
<li>A text component which aligns the itself inside the rectangle</li>
<li>A hover effect  when mouse comes over the button</li>
<li>A simple action fucntion which is invoked when the mouse clicked</li>
</ol>
I first extended the CustomNode and named my class ButtonFX<br />
<pre class="brush:javafx">
public class ButtonFX extends CustomNode{</pre>
<br />
then I override the create() function, which returns node , in this case, the custom button<br />
I here should mention that Group is a collection of node elements and itself is a node so I will be returning group component which consist of rectangle  and text<br />
here is code for Rectangle<br />
<pre class="brush:javafx">
rect = Rectangle {
             width: 60, height: 30
             fill: bind if(rect.hover) Color.BLACK else Color.BLUE
             stroke:Color.WHITE
             arcHeight:10
             arcWidth:10
         }</pre>
<br />
here  the fill variable in  line 3 uses hover keyword to control the color of rectangle, I assigned rect so that I could later use hover keyword<br />
<br />
arcHeight and arcWidth are used to provide some visual appeal to button<br />
<br />
here is text class which is more interesting<br />
<br />
<pre class="brush:javafx">
Text {
 font : font =Font {
                 size: 14
              }
 y: rect.layoutBounds.minY+
                  (rect.layoutBounds.height - font.size)/2,
 x: rect.layoutBounds.minX+5
 content: "Login"
 textOrigin:TextOrigin.TOP
 textAlignment:TextAlignment.CENTER
 fill:Color.WHITE
}</pre>
<br />
The important part of this is the y constraint, here a formulae is used to align it to the center of rectangle based on font size and rectangle size<br />
now we know why reffering to rectangle as rect come in handy , layoutBounds allow us to access dimension (x position y position , width, height etc.,) and for action functionality I created a function which simply prints that button is clicked , this should be overridden when we call ButtonFX to mimic proper button functionality<br />
<br />
<h3>
here is full code</h3>
<br />
<pre class="brush:javafx">
/*
 * ButtonFX.fx
 *
 * Created on 7 May, 2009, 6:51:18 PM
 */

package nbtalkfx;


import javafx.scene.CustomNode;
import javafx.scene.Group;
import javafx.scene.input.MouseEvent;
import javafx.scene.Node;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.scene.text.Font;
import javafx.scene.text.Text;
import javafx.scene.text.TextAlignment;
import javafx.scene.text.TextOrigin;
import javafx.scene.effect.Reflection;
import javafx.scene.text.FontWeight;
import javafx.scene.effect.Glow;

/**
 * @author Vaibhav Mishra
 */

public class ButtonFX extends CustomNode{
    var rect:Rectangle;
    var font:Font;
    var text:Text;
    package var clicky:function() ;
//public function clickAction():Void{
//        println("buttonFX");
//    }

    override function create():Node{
        Group{
            content:[
                rect = Rectangle {
                    width: 60, height: 30
                    fill: bind if(rect.hover) Color.BLACK else Color.LIGHTGRAY
                    stroke:bind if(rect.hover) Color.WHITE else Color.GRAY
                    arcHeight:10
                    arcWidth:10
                    strokeWidth:3
                }
                text = Text {
                    id:"loginButtonText"
                    font : font =Font {
                        size: 18
                        embolden:true
                    }
                    y: rect.layoutBounds.minY+(rect.layoutBounds.height - font.size)/2, 
                    translateX: bind rect.layoutBounds.minX +(rect.layoutBounds.width/2) - (text.layoutBounds.width/2)

                    content: "Login"
                    textOrigin:TextOrigin.TOP
                    //textAlignment:TextAlignment.CENTER
                    fill:bind if(rect.hover) Color.WHITE else Color.BLACK
                    //layoutBounds:rect.layoutBounds
//                    effect :Glow {
//                    level: 1.0
//                }
                }
            ]
            onMouseClicked:function (e:MouseEvent):Void{
                println("button clicked");
                clicky();
            }
            effect:Reflection {
                      fraction: 0.25
                      topOffset: 0.0
                      topOpacity: 0.5
                      bottomOpacity: 0.0
                   }

        }
    }
}
</pre>
<br />
<br />
</div>

**update**: overriding functions defined in Custom components gives compilation error in current openjfx compiler 1.1.1 , this seems to be fixed in version 1.2 or later,  I have not implemented it here , will do it after javaone.<br />

**update2**: the default javafx brush i am using for blogger doesnot wrap code automatically and some part of line y part of text is missing in display, view source to check full code .<br />

**update3**: I found a way to do it thanx to dynamic Sun community, now I have changed the full working code
