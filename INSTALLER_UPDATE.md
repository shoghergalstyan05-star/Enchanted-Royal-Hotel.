# Install the new section beside an existing castle

Use the castle meshes already imported into your place. This update contains installation helpers, not replacement art. The original milestone ZIP is unchanged.

1. Click the red **Stop** square at the top-left of Studio. Installation must happen in Edit mode.
2. Check that the imported model directly under Workspace is named **ERH_ImportedMeshes** and still contains all 213 original ERH_Chunk mesh names.
3. Open **InstallFrontSlice_BesideExistingMap.lua** from this update using TextEdit. Press **Command+A**, then **Command+C**.
4. Click inside the Studio Command Bar, replace the previous measurement command with the copied installer, and click the **Run** button beside that command box. Do not use the top-left Play button to execute the command.
5. Look for **[ERH INSTALLED]** in Output. Click inside the 3D viewport and press **F** to frame the selected new section. Then press Play to check the new lobby arrival.

The installer measures the existing RoyalHotelMap and puts the new section 20 studs beyond the rightmost of its parts. It restores every imported mesh to its authored size and position, assigns the supplied colors/materials, and builds the supplied invisible collision. A raycast under the old LobbySpawn determines the floor height before any visible change. It stops if required map objects, uploaded mesh IDs, protected configuration, or floor support are missing. The original fallback-map placement and bridge are retained when no existing map is present.

The existing map, room IDs, gameplay scripts, diamonds, Royal Egg price of 750, and saved-data configuration are retained. Only LobbySpawn moves to the new foyer. The existing Royal Map destinations still point into the old map. A physical walk connection between the staged section and the old castle remains to be authored.

After inspecting the result, stop Play and run **ReadOnlyAudit.lua** in the Command Bar. Continue with the original package's **docs/STUDIO_PLAYTEST.md** before saving a reviewed result. Offline validation does not establish successful Studio import, movement, teleports, or persistence.

To reverse installation, stop Play and run **RollbackFrontSlice.lua**. It restores the previous imported mesh transforms and flags and the old LobbySpawn transform; it does not delete the old castle.
