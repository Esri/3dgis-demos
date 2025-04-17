This app demonstrates how you can use 3D object layers to make a system of record accessible through the web.

## Featured capabilities

- Filter buildings by time
- Download buildings and terrain as glTF
- Upload a new proposed building design
- Perform a client-side viewshed analysis on the new building

## Resources

- Recording of the demo: [UC2024 - Urban change over time.mp4](https://esriis-my.sharepoint.com/:v:/g/personal/arno9993_esri_com/Ec3BCTicweJIqinwY6XfcFABuDE1JKPbVj5aqvVEWxFy-g)
- 3D assets used in demo
  - Blender project: [development-site.blend](https://github.com/Esri/3dgis-demos/raw/refs/heads/main/demos/urban-change-over-time/development-site.blend)
  - Upladed building proposal: [building-proposal-v1.glb](https://github.com/Esri/3dgis-demos/raw/refs/heads/main/demos/urban-change-over-time/building-proposal-v1.glb)
- Source code is available on GitHub: [https://github.com/Esri/3dgis-demos](https://github.com/Esri/3dgis-demos/tree/main/demos/urban-change-over-time)

## Steps

Web scenes and 3D layer types now support time, helping us to look at the past and future. Let’s bring in a time slider and start in the year 1200, where we see that one of the churches is the oldest building still present in Zurich

![Time Enablement](https://www.arcgis.com/sharing/content/items/30bd624de45247dfa53320a8213729a4/resources/screenshots/01-time-enablement.png)

Moving forward in time we see individual buildings coming in, until the present when we will also bring in the latest tree dataset. This scene layer also contains planned development visualized by massing volumes, allowing us to see how the city will change in the next few years.

Let’s zoom into one of these plans and assume we are an architect that wants to design the new building. Scene layer editing is now fully supported in the web, allowing us to upload, but also download 3D models. This allows an architect to bring the surroundings around the planned development into our 3D modeling software of choice.

![Download 3D Buildings and Terrain](https://www.arcgis.com/sharing/content/items/30bd624de45247dfa53320a8213729a4/resources/screenshots/02-download-3d-data.png)

We can now import the exported glTF in our modeling software and use the terrain and contextual buildings to create a new design proposal. Using the editor we can upload it back into the ArcGIS system and place the building at the correct location using tooltips. Several formats besides glTF are supported, such as OBJ, FBX, Collada and IFC and get converted on the server side to I3S for efficient streaming.

![Upload Building](https://www.arcgis.com/sharing/content/items/30bd624de45247dfa53320a8213729a4/resources/screenshots/03-upload-building.png)

Once the building is persisted, the footprint of the new building is queried to filter existing buildings in our scene layer or flatten an integrated mesh layer to visualize it in a realistic context.

![Realistic Visualization](https://www.arcgis.com/sharing/content/items/30bd624de45247dfa53320a8213729a4/resources/screenshots/04-realistic-visualization.png)

The building in front used to be a local brewery that got transformed into a public bath with a rooftop pool, one of Zurich’s highlights for locals and visitors.

Using a client-side viewshed analysis, I can now for example see what parts of my new building can be seen from this public rooftop location.

![Viewshed Analysis](https://www.arcgis.com/sharing/content/items/30bd624de45247dfa53320a8213729a4/resources/screenshots/05-analysis.png)

This demo showed how to visualize, upload and analyze change using a 3D Object Layer.
