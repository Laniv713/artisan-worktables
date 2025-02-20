# Configuration Files

To give you an idea of Artisan Worktables' configuration options, here is an up-to-date display of the available config files and their default values.

## Toolbox

`config/artisanworktables/artisanworktables.module.Toolbox.cfg`

```coffeescript
# Configuration file

general {
    # Set to false to disable the toolbox.
    B:ENABLE_MODULE=true

    toolbox {
        # Set to false to remove the toolbox.
        B:ENABLED=true

        # Set to false to prevent the toolbox from keeping its contents when broken.
        B:KEEP_CONTENTS_WHEN_BROKEN=true

        # Set to false to allow any item to be placed into the toolbox.
        # If set to true, only tools that are part of any worktable recipe may be stored in the toolbox.
        B:RESTRICT_TO_TOOLS_ONLY=true
    }

    mechanical_toolbox {
        # Set to false to remove the mechanical toolbox.
        B:ENABLED=true

        # Set to false to prevent the mechanical toolbox from keeping its contents when broken.
        B:KEEP_CONTENTS_WHEN_BROKEN=true

        # Set to false to allow any item to be placed into the mechanical toolbox.
        # If set to true, only tools that are part of any worktable recipe may be stored in the mechanical toolbox.
        B:RESTRICT_TO_TOOLS_ONLY=true
    }

}
```

## Tools

`config/artisanworktables/artisanworktables.module.Tools.cfg`

```coffeescript
# Configuration file

general {
    # To disable a tool type, remove it from this list.
    # If new tool types are added to the mod, you may have to regenerate your config file
    # or manually add them to this list to activate them.
    S:ENABLED_TOOL_TYPES <
        artisans_cutters
        artisans_hammer
        artisans_framing_hammer
        artisans_handsaw
        artisans_cutting_board
        artisans_pan
        artisans_beaker
        artisans_burner
        artisans_driver
        artisans_spanner
        artisans_lens
        artisans_sifter
        artisans_gemcutter
        artisans_pliers
        artisans_athame
        artisans_grimoire
        artisans_chisel
        artisans_trowel
        artisans_carver
        artisans_razor
        artisans_compass
        artisans_quill
        artisans_needle
        artisans_shears
        artisans_punch
        artisans_groover
        artisans_mortar
        artisans_knife
     >

    # Set to false to disable all tools.
    # This supersedes all other tool settings.
    B:ENABLE_MODULE=true

    # Set to false to prevent creation of ore dict groups for tools by material type, ie. 'toolFlint' or 'toolCopper'.
    B:ENABLE_TOOL_MATERIAL_ORE_DICT_GROUPS=true

    # Set to false to disable all tool recipes.
    B:ENABLE_TOOL_RECIPES=true

    # Set to false to prevent creation of ore dict groups for tools by type, ie. 'artisansHammer' or 'artisansChisel'.
    B:ENABLE_TOOL_TYPE_ORE_DICT_GROUPS=true

    # Change the ore dict prefix for each tool material type group.
    # This is used when generating the tool material .json file.
    # Changing this will have no effect if the 'Custom' tool material file has already been generated.
    # You will need to regenerate the file by deleting it and running the game, or manually change the file.
    S:TOOL_BY_MATERIAL_ORE_DICT_PREFIX=artisansTool

    # Change the ore dict prefix for each tool type group.
    S:TOOL_BY_TYPE_ORE_DICT_PREFIX=artisans

    client {
        # Set to false to disable the durability tooltip on tools from this mod.
        B:ENABLE_DURABILITY_TOOLTIP=true
    }

}
```

## Worktables

`config/artisanworktables/artisanworktables.module.Worktables.cfg`

```coffeescript
# Configuration file

general {
    # Set to true to enable log warnings for duplicate recipe names.
    # If you're using a lot of your own recipe names, you can enable this
    # from time to time to check that you haven't accidentally used the
    # same name twice.
    B:ENABLE_DUPLICATE_RECIPE_NAME_WARNINGS=false

    # Set to false to disable workshops.
    B:ENABLE_WORKSHOPS=true

    # Set to false to disable workstations.
    B:ENABLE_WORKSTATIONS=true

    # Set to false to disable worktables.
    B:ENABLE_WORKTABLES=true

    # If set to true, crafting tools must have sufficient durability remaining to perform the craft.
    # If set to false, this restriction is ignored.
    B:RESTRICT_CRAFT_MINIMUM_DURABILITY=true

    ##########################################################################################################
    # enable_table_type
    #--------------------------------------------------------------------------------------------------------#
    # Set to false to selectively disable a table type across all table tiers.
    ##########################################################################################################

    enable_table_type {
        B:basic=true
        B:blacksmith=true
        B:carpenter=true
        B:chef=true
        B:chemist=true
        B:designer=true
        B:engineer=true
        B:farmer=true
        B:jeweler=true
        B:mage=true
        B:mason=true
        B:potter=true
        B:scribe=true
        B:tailor=true
        B:tanner=true
    }

    ##########################################################################################################
    # fluid_capacity_worktable
    #--------------------------------------------------------------------------------------------------------#
    # Worktable fluid capacity (milli-buckets).
    ##########################################################################################################

    fluid_capacity_worktable {
        I:basic=4000
        I:blacksmith=4000
        I:carpenter=4000
        I:chef=4000
        I:chemist=4000
        I:designer=4000
        I:engineer=4000
        I:farmer=4000
        I:jeweler=4000
        I:mage=4000
        I:mason=4000
        I:potter=4000
        I:scribe=4000
        I:tailor=4000
        I:tanner=4000
    }

    ##########################################################################################################
    # fluid_capacity_workstation
    #--------------------------------------------------------------------------------------------------------#
    # Workstation fluid capacity (milli-buckets).
    ##########################################################################################################

    fluid_capacity_workstation {
        I:basic=8000
        I:blacksmith=8000
        I:carpenter=8000
        I:chef=8000
        I:chemist=8000
        I:designer=8000
        I:engineer=8000
        I:farmer=8000
        I:jeweler=8000
        I:mage=8000
        I:mason=8000
        I:potter=8000
        I:scribe=8000
        I:tailor=8000
        I:tanner=8000
    }

    ##########################################################################################################
    # fluid_capacity_workshop
    #--------------------------------------------------------------------------------------------------------#
    # Workshop fluid capacity (milli-buckets).
    ##########################################################################################################

    fluid_capacity_workshop {
        I:basic=16000
        I:blacksmith=16000
        I:carpenter=16000
        I:chef=16000
        I:chemist=16000
        I:designer=16000
        I:engineer=16000
        I:farmer=16000
        I:jeweler=16000
        I:mage=16000
        I:mason=16000
        I:potter=16000
        I:scribe=16000
        I:tailor=16000
        I:tanner=16000
    }

    client {

        ##########################################################################################################
        # text_highlight_color
        #--------------------------------------------------------------------------------------------------------#
        # Here you can change the gui text highlight color. (Hexadecimal)
        ##########################################################################################################

        text_highlight_color {
            S:basic=bc9862
            S:blacksmith=a2a2a2
            S:carpenter=bc9862
            S:chef=ffffff
            S:chemist=476147
            S:designer=ffffff
            S:engineer=ca671b
            S:farmer=80c652
            S:jeweler=695985
            S:mage=ac51e3
            S:mason=979797
            S:potter=b75a40
            S:scribe=b6884f
            S:tailor=ac51e3
            S:tanner=c77d4f
        }

    }

    pattern {
        # Set to false to disable pattern creation for workshops.
        B:ENABLE_PATTERN_CREATION_FOR_WORKSHOPS=true

        # Set to false to disable pattern creation for workstations.
        B:ENABLE_PATTERN_CREATION_FOR_WORKSTATIONS=true

        # Set to false to disable pattern creation for worktables.
        B:ENABLE_PATTERN_CREATION_FOR_WORKTABLES=true

        # Set to false to prevent players from sneak-clicking to clear the patterns.
        # This is useful if you want to provide your own method for clearing patterns.
        B:ENABLE_SNEAK_CLICK_TO_CLEAR=true
    }

}
```