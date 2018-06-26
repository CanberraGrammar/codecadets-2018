---

title: Unity terrain

---


## The goal: build a natural terrain environment

Many games incorporate outdoor environments, they may look difficult but they are surprisingly easy to create in unity.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/0_nature.jpg" alt="nature" style="width: 100%;"/>

## Generating Terrain

See weeks [6 and 7 lab](unitylevel.md).

You should have something that looks vaguely like this.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/1_blank_terrain.PNG" alt="blank terrain" style="width: 100%;"/>

## Import assets

In order to make your dull grey terrain look natural, you need textures. For this exercise we will use the sample unity textures, but remember you are free to download textures from the asset store.

`TO-DO` import assets from the assets menu: Navigate to `Assets > Import Package > Environment`

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/2_environment_assets.png" alt="assets" style="width: 100%;"/>

Click import in the pop-up window

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/3_import.png" alt="import" style="width: 100%;"/>

## Texture the Terrain

Select your terrain by clicking on it, then look at the inspector on the right.

`TO-DO` edit ground textures by clicking the `Edit Textures` button.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/4_edit_textures_button.PNG" alt="edit textures" style="width: 100%;"/>

Click on `add texture`, then one of the `select` squares. Search for grass, you should see a grass texture, this one will cover the entire terrain by default. If you want your primary ground texture to be something like sand, add that one first as it will cover the whole terrain.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/5_add_texture.png" alt="add textures" style="width: 100%;"/>

Add more than one texture for variety, in this example there is grass and sand but you may find more to use.

`TO-DO` use an alternate texture to create variety in your terrain. Select the `Paint Texture` tool and choose a brush, then you can paint that texture on your terrain.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/6_texture_paint.PNG" alt="paint textures" style="width: 100%;"/>

## Add Trees to your Scene


To further diversify your terrain, you may wish to add trees to make a forrest.

`TO-DO` select the `Paint Trees` tool and add a tree texture by clicking the `Edit Trees` button.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/7_edit_trees.PNG" alt="tree textures" style="width: 100%;"/>

Click on the small dot to select a tree texture. Then click `Add`.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/8_select_tree.png" alt="select tree" style="width: 100%;"/>

Paint trees onto your terrain, play with the `brush size` and `tree density` options for different effects.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/9_paint_trees.PNG" alt="pint trees" style="width: 100%;"/>

## Add Extra Details

`TO-DO` add extra detail to your terrain with grass. Click on the `Paint Details` tool, then the `Edit Details` button.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/10_edit_details.PNG" alt="select details" style="width: 100%;"/>

Click the small dot and select a grass texture, you can search for 'grass' to see all the options.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/11_select_grass.png" alt="select grass" style="width: 100%;"/>

Paint grass onto your terrain, you have to close to it to be able to see it, as the render distance is quite low.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/12_paint_grass.PNG" alt="paint textures" style="width: 100%;"/>

-----

## Bonus Activity: Adding collision to your world and objects

Start by selecting your terrain in the Hierarchy menu. Follow to the top bar, and select

```
Component -> Physics -> Terrain Collider
```

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/TerrainCollider.png" alt="Adding collision to your ground" style="width: 100%;"/>

The properties of the terrain collider will appear over in the inspector for your terrain.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/TerrainCollider_2.png" alt="It appears over here" style="width: 100%;"/>

Next, add two things to your object in the world. Select your object, and go to the physics menu again and add these two things.

* Rigidbody Physics. These will apply gravity to your object, and you can change the properties of the object's mass in the inspector on the right.

* An appropriately shaped collider. Box will work for more objects, but if you have a different shape like a ball you would want a sphere. This will stop your falling object from just phasing through the floor.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/ObjectColliders.png" alt="Add collision to your objects" style="width: 100%;"/>


If done correctly, your object should fall naturally and stop on the ground like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/unityterrain/Gravity.gif" alt="falling firetruck" style="width: 100%;"/>
