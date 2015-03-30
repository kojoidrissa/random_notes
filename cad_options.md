#CAD software options
##NOTE: Combine this with the [3D_printing.md] file in this repo
-  [FreeCAD](http://www.freecadweb.org); FLOSS [parametric modeling](http://en.wikipedia.org/wiki/Parametric_model) software. I've got a PACKT book on this, [`FreeCAD[HOWTO]`](http://www.amazon.com/FreeCAD-How-Daniel-Falck/dp/1849518866). It's got TERRIBLE reviews on Amazon and Chris Kelley hates it. But the ebook was SUPER cheap (esp. at 60% off) and it's got a Python API. So, I'll give it a look.
    +  It could also be a project I [contribute](http://www.freecadweb.org/wiki/index.php?title=Help_FreeCAD) to.
+  [Blender](http://www.blender.org): Open-Source 3D modeling software scriptable in Python
    *  [3D printing toolkit](http://wiki.blender.org/index.php/Extensions:2.6/Py/Scripts/Modeling/PrintToolbox)
    *  [Google Search: "blender python 3d printing" ](https://www.google.com/search?client=safari&rls=en&q=blender+python+3d+printing&ie=UTF-8&oe=UTF-8)
    *  [PyCon 2015 Talk: "3D Print Anything with the Blender API"](https://us.pycon.org/2015/schedule/presentation/352/)
        -  Reading that description tells me Blender's Python API must be fairly awesome
        -  Same speaker is also doing [Intro to 3D Graphics with Blender and the Blender API](https://us.pycon.org/2015/schedule/presentation/307/)
+  [TinkerCAD](https://www.tinkercad.com), which I just started using on 2015-03-29, trying to recreate the Exo-Exodus logo. Wanjun uses it in her [3D Printing for Young Designers](https://txrxlabs.org/classes/164/3d-printing-for-young-designers/) class.

##CAD background Research
Results from stuff I was doing at the lab on 2015-03-29 and conversations with Mark Sullivan and Patrick Wheeler.

-  [CSG](http://en.wikipedia.org/wiki/Constructive_solid_geometry) vs [BREP](http://en.wikipedia.org/wiki/Boundary_representation)
    +  CSG gets used in FLOSS software more often, probably because it's easier to implement. However, BREP is better for more complex shapes.
    +  [Open Cascade](http://en.wikipedia.org/wiki/Open_Cascade_Technology) is an Open Source BREP [geometric modeling kernel](http://en.wikipedia.org/wiki/Geometric_modeling_kernel)
        *  their [homepage](http://www.opencascade.org)
        *  [Open CASCADE Technology](http://dev.opencascade.org), the dev site
        *  [Open CASCADE Community Edition](https://github.com/tpaviot/oce) Github repo
        *  [PythonOCC](http://www.pythonocc.org) is a Python wrapper for Open CASCADE. It's also mentioned in the [Open CASCADE forums](http://www.opencascade.org/org/forum/?forum=16). It's got a VERY interesting [feature set](http://www.pythonocc.org/category/features_overview/).
            *  It's  web-ready via THREE.js (I was just reading about that lib in the 3D Javascript book I got from Amanda)
            *  Cross-platform (OSX, Linux, Windows)
            *  will import/export most standard engineering files like STL & VRML(the two I'm most interested in) 
-  [Z3](https://github.com/Z3Prover/z3) is *a high-performance theorem prover being developed at Microsoft Research.* It's available under an MIT license. I'm not 100% sure how this fits in, but Patrick & Mark found it quite interesting. But, the existence of Open CASCADE seems to make it less needed for BREP CAD purposes. But, you know, if you need some other theorems proved...they've got you covered, I'd assume.
