# Godot 4 C# Exports
A Godot 4 Node Exporter to the editor, letting you place your nodes with attached C# scripts easier.

# Built from an old repository.
Code was heavily referenced and built from [this repository](https://github.com/m50/Godot-CSharp-Node-Exports). I simply reworked some of it to work in Godot 4.

# Installation
Setup the resource in the `res://addons/` directory and it should work fine, you may need to go to your project settings to setup the plugin. Building will make the Plugin assemble your types.

Usage
-----
* `<Class Attribute> InstantiableAttribute : Attrbiute` Marks the class to appear in the editor.
* `<Class Attribute> IconAttrbiute : Attribute` Gives the class an icon in the editor.

# Examples
```CS
using Godot;
using Plugins.CSExports;

namespace MyGame
{
	[Instantiable]
	[Icon("res://MyIcon.svg")]
	public partial class ExampleClass : Node3D
	{
		public override void _Ready()
		{
			GD.Print("Hello World!");
		}
	}
}
```
