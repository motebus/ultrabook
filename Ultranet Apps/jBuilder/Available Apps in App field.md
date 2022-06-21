## Available Apps in App field 
### Directly enter page://xxx of App you want to use in the 'App' field 
  - **page://url** 
    * Params field: `{"url":"https://your-url","scroll":true}` 
  - **For url of youtube**
     - Directly enter the Youtube url of your video into the App Field.<br>
     - NOTE:
      1. Use the standard address bar url, e.g. https://www.youtube.com/watch?v=VIDEOID.
      2. Other formats sych as the video sharing link https://youtu.be/VIDEOID, or playlist links will not work in panel-frames. 
      3. Leave the parameter field blank
  - **page://image**
    * Params field: `{"url":"https://your-image-url"}`
     - NOTE: 
      1. By default, if the actual image size is larger than its panel size, the image will be resized to fit the panel, potentially having an additional border around the image. 
      2. If your image is smaller than the panel, the border around it may end up quite large (depends on panel size). 
      3. To make your image scale automatically to fill the panel (stretch and take up as much space as possible, disregarding aspect ratio), add `,"fullwidth":1` into the Params field. 
  - **page://slider** (currently maitaining)
    * Params field: `{"json":["https://your-image-url","https://your-image-url",..."https://your-image-url"]}` 
  - **Charts**<br> (currently maitaining)
    Currently there are 6 available chart types: bar, hbar, line, linearea, pie and circle. 
    1. Type `page://chart` into the App Field
    2. Enter into the Data Field: 
       > {"chart":{"type":"line","title":"Sample Chart","data":{"columns":[{"type":"x","field":"field name","name":"Course name"},{"type":"y","field":"numerical weight","name":"measured aspect"}],"rows":[{"numerical weight":450,"field name":"A"},{"numerical weight":350,"field name":"B"},{"numerical weight":300,"field name":"C"},{"numerical weight":370,"field name":"D"},{"numerical weight":400,"field name":"E"}]}}}
    3. Replace ”type”,“numerical_weight”, “field_name” and other content to customise your chart.
       ![](https://i.imgur.com/Rht0Sxn.png)
       https://git.page/jj/board?qname=chart for charts demo. In jBuilder, search in the Public board list for `chart`. Select the board with the qname `chart` and qcode `1604544476104`.
       Other Samples:
       - QName= chartpractice, QCode=1611802967946
       - QName=011121, QCode=1610357672283
   - **Bricks** (currently unavailable)<br>
    1. Type`page://url` into the App Field.
    2. Enter `{"url":"https://xxx"}` into the Params field, replacing `https://xxx` with the url of the brick.
    See the jboard with the QName jbrick and go to https://git.page/jj/board?qname=jbrick for bricks demo. <br>
    ![](https://i.imgur.com/xXEWyUx.png)
    
    
 #### Dashboard panels customised with fBuilder (currently unavailable)
  - **Cloud Room Display** 
    * Type `page://room` into the App Field and enter `{"tag":"TAG"}` into the Params field, replacing `TAG` with your own room flow tag or 
    * Type `page://panel` into the App Field and enter `{"tag":"TAG"}` into the Params field, replacing `TAG` with your own panel flow tag. 
  - **View (log)**
    1. Create a flow in fbuilder and set the destination to your view name 
    2. Type `page://view` into the App Field.
    3. Enter `{"tag":"<VIEW>"}` into the Params field, replacing `VIEW` with your view name.
  - **Header** 
    1. Type `page://header` into the App Field.
    2. Enter `{"title":"TITLE","logo":"https://xxx"}` into the Params field, replacing `TITLE` with the title you want for the header and `https://xxx` with the url of the logo icon. 
  - **Kanban**
    1. Type `page://kanban` into the App Field.
    2. Enter `{"tag":"YourTAG"}` into the Params field, replacing `YourTAG` with your kanban name.
