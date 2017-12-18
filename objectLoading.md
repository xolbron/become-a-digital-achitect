# Loading 3D Models into A-Frame
*A Guide written by Jerome Foster II, 18 March, 2017*

## Introduction


Let's say that you want to load yor favorite pokemon into VR so that all of your freinds can see it. The obj-model component loads a 3D model using a Wavefront (.OBJ) file, a .MTL file, and some pictures.


## Where do you find Wavefront Online 

- [Clara.io](https://clara.io/) - A Repository of 3D models.
- [Sketchup](https://3dwarehouse.sketchup.com/) - Repository of models.
- [Blender](https://www.blender.org/) - A free open-source 3D modeling program with plenty of existing learning resources to create models.
- [Sketchfab](https://sketchfab.com/?utm_source=emails&utm_medium=drip&utm_campaign=welcome)- publish, create, and discover 3D content online and in VR.
- [Maya](https://www.autodesk.com/products/maya/overview) - 3D animation, modeling, simulation, and rendering software provides an integrated, powerful toolset. Use it for animation, environments, motion graphics, virtual reality, and character creation.
- [Character Generator](https://www.autodesk.com/products/character-generator/overview) - Create custom and ready-to-animate 3D characters with Character Generator web-based tools. Control a character’s body, face, clothes, and hair. Generate rigged character models for use in animation packages and game engines.



## How to Download a .Obj-Model

### Pre-loading Files

We can load an .OBJ model by making an `<a-assets>` area that loads the obj and mtl files before you call the path to an .OBJ and .MTL file.

```html
<a-scene>

  <a-assets>
    <a-asset-item id="tree-obj" src="/path/to/tree.obj"></a-asset-item>
    <a-asset-item id="tree-mtl" src="/path/to/tree.mtl"></a-asset-item>
  </a-assets>

  <a-entity obj-model="obj: #tree-obj; mtl: #tree-mtl"></a-entity>

</a-scene>
```


### Loading Inline

- **Copy File Path**: In order to properly load the different files you must right click the file and click the button that says `copy file path`.


```html
<a-entity obj-model="obj: url(/path/to/tree.obj); mtl: url(/path/to/tree.mtl)"></a-entity>
```

### The .MTL File
- The .mtl is a file that is a 3 dimensional shape
- These files cannot be loaded into the [Thimble](https://thimble.mozilla.org/en-US/) IDE, but can be in [Cloud 9](https://c9.io) 



## Troubleshooting Commmon Problems

- **Model not appearing:** If you don’t see your model, try scaling it down. OBJ models vertices commonly have large scales of units in comparison to A-Frame’s unit of meters.

- **Does not have .mtl file or .obj:** If your code does not project either an .obj file or .mtl file that means that it was not donr the right way.