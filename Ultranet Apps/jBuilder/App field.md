## App field 

### Directly enter page://xxx of App you want to use in the 'App' field 

---
- **page://url** 
    * Params field: `{"url":"https://your-url","scroll":true}` 

- **For url of youtube**

     - Directly enter the Youtube url of your video into the App field.

     - NOTE:

     1. Use the standard address bar url, e.g. https://www.youtube.com/watch?v=VIDEOID. <br>
        Other formats sych as the video sharing link https://youtu.be/VIDEOID, or playlist links will not work in panel-frames. 

     2. Leave the parameter field blank

     3. Alternative way to add multiple Youtube videos: create a [TV channel](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/jBuilder/How%20to/Create%20a%20TV%20channel%20on%20Dock.md) on Dock Builder

---
- **page://image**

    * Params field: `{"url":"https://your-image-url"}`

     - NOTE: 

     1. By default, if the actual image size is larger than its panel size, the image will be resized to fit the panel, potentially having an additional border around the image. 

     2. If your image is smaller than the panel, the border around it may end up quite large (depends on panel size). 

     3. To make your image scale automatically to fill the panel (stretch and take up as much space as possible, disregarding aspect ratio), add `,"fullwidth":1` into the Params field. 

---
- **page://slider**
    * Params field: `{"json":["https://your-image-url","https://your-image-url",..."https://your-image-url"]}` 

---
- **page://tg**

    * Params field: see [TG Params field.md](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/jBuilder/TG%20Params%20field.md)

---

### Currently unavailable Apps

- **page://chart** (maitaining)

    * Available Chart types: bar, hbar, line, linearea, pie and circle. 

    * Data Field: 
       > {"chart":{"type":"line","title":"Sample Chart","data":{"columns":[{"type":"x","field":"field name","name":"Course name"},{"type":"y","field":"numerical weight","name":"measured aspect"}],"rows":[{"numerical weight":450,"field name":"A"},{"numerical weight":350,"field name":"B"},{"numerical weight":300,"field name":"C"},{"numerical weight":370,"field name":"D"},{"numerical weight":400,"field name":"E"}]}}}

    * Replace ”type”,“numerical_weight”, “field_name” and other content to customise your chart.

       ![](https://i.imgur.com/Rht0Sxn.png)

       https://git.page/jj/board?qname=chart for charts demo. In jBuilder, search in the Public board list for `chart`. Select the board with the qname `chart` and qcode `1604544476104`.

       Other Samples:

       - QName= chartpractice, QCode=1611802967946
       - QName=011121, QCode=1610357672283

---
- **page://url (bricks)** (unavailable)

    * Params field: `{"url":"https://your-brick-url"}` 

    * See the jboard with the QName jbrick and go to https://git.page/jj/board?qname=jbrick for bricks demo.
    ![](https://i.imgur.com/xXEWyUx.png)
    
---

 #### Dashboard panels customised with fBuilder (unavailable)

- **page://room or page://panel** (Cloud Room Display)

    * Params field: `{"tag":"TAG"}` , replace `TAG` with your own room/panel flow tag

---
- **page://view**(log)

    1. Create a flow in fbuilder and set the destination to your view name 
    * Params field: `{"tag":"<your-view-name>"}`

---
- **page://header** 

    *  Params field: `{"title":"<title-you-want>","logo":"https://your-logo-url"}`

---
- **page://kanban**

    * Params field: `{"tag":"<your-kanban-name>"}` 
