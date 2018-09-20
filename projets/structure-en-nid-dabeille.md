# Structure en nid d'abeille

## 

Petit script en openscad pour générer des structures en nid d'abeille

![](../.gitbook/assets/image%20%2847%29.png)

![](../.gitbook/assets/image%20%286%29.png)





{% code-tabs %}
{% code-tabs-item title="CellArray3D.scad" %}
```text

cells= [
[1,0,1,0,1],
 [1,1,1,0,1],
[1,0,0,1,1],
 [1,0,1,0,0],
];
 
cellArray3D(cells,r=10, filled=true);
 
module cellArray3D(cells,r=30,th=1.5, filled= true, h = 18)
{
     union()
    {
        translate([-40,-30]){
            linear_extrude(height= h-th)
                    cellArray(cells ,r,th,false);
            translate ([0,0,-th]) linear_extrude(height=th)  
                    cellArray(cells ,r,th,filled);
        }
    }
}
 
function cellWidth(r) = 2*cos(30)*r;
module cellArray(cells, r=30,th=3, filled= false)
{
    innerCellRadius= r - th/2;
 
   //Move boundingbox to 0,0
    translate([0.5*cellWidth(r),r,0])
    {
        for(lineNumber = [0:len(cells)-1])
        {
            for (i = [0:len(cells[lineNumber])-1])
            {
                if(cells[lineNumber][i] ==1)
                {
                   if( lineNumber %2 == 0)
                    {    
                        translate([cellWidth(innerCellRadius)*i,lineNumber*innerCellRadius*1.5,0]) 
                            cell(th,r,filled);
                    }
                    else
                    {            
                        translate([cellWidth(innerCellRadius)*(i+0.5), innerCellRadius*lineNumber*1.5,0]) 
                            rotate([0,0,60])cell(th,r,filled);
                    }
                }
            }       
        }
    }
}
 
module cell(th=2,r=10,filled =false)
{
    rotate([0,0,30]) difference()
    {
        circle($fn=6,r=r,center=false);
        if(! filled)
        {
            circle($fn=6,r=r-th,,center= false);
        }
    }
}

```
{% endcode-tabs-item %}
{% endcode-tabs %}

