# Lifecycle Events
When starting, FML and with it Minecraft go through several stages. On this page we will cover what you should do when during the main stages: PreInitialization, Initialization, PostInitialization and ServerStarting.
Some things should be done on the client only. These usually involve graphical components, like models or GUIs. These actions are marked with *italic text*.

Why should you follow these conventions? It ensures that your mod is working as expected, and increases cross-mod compatibility.
You will notice that most things are done during PreInit. In general it is advisable to do everything as early as possible so that any mod requiring data from other mods can depend on it. For example all items having been registered before Initialization to perform an action on it.

## PreInitialization
This is the FMLPreInitializationEvent. Here you should:
* register your Items
* register your Blocks
* register your Tile Entities
* register your Entities
* register your Network Channels and Messages
* oredict your Items and Blocks
* *register Model mappings*

## Initialization
This is the FMLInitializationEvent. Here you should:
* add Recipies

## PostInitialization
This is the FMLPostInitializationEvent. Here you should:
* register Forge Event Handlers

## Server Starting
This is the FMLServerStartingEvent. Here you should:
* register commands via the event