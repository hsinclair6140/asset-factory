Creating a Package
==================

Packages created in the Asset Factory are nuget packages that contain .uasset files. This page provides information on how to create these packages.

Dependencies
------------

* `Nuget <https://www.nuget.org/downloads>`_.

Procedure
---------
1. Create a .nuspec file for the .uasset, for example:

 .. code-block:: xml

    <?xml version="1.0" encoding="utf-8"?>
    <package>
        <metadata minClientVersion="3.3">
            <id>AssetFactory.SFX.Ambient.Dark.Hostile</id>
            <version>1.0.0</version>
            <title>AssetFactory SFX Ambient Dark Hostile</title>
            <authors>Heath Sinclair</authors>
            <description>AssetFactory SFX Ambient Dark Hostile</description>
            <contentFiles>
                <files include="Hostile.uasset" />
            </contentFiles> 
        </metadata>
    </package>

2. Open a Command Prompt Window.
3. Navigate to the directory with the .nuspec file.
4. Issue the following command:

 .. code-block:: console

    nuget pack

5. Upload the newly created nuget package to the Nexus Repository.