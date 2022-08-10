# NAWCAD-WOLF-VR-TOURS

This is a demo that includes assets scripts, photosheres, etc that can be used to create a Google Cardboard based tour more smoothly.


# Gaze Interactor Prefabs
This is the folder that contains all the assets that will allow the player to interact with the enviroment.

The Gaze Interaction Prefabs Folder has the following  prefabs
  - Demo: which contains an example demo on how the gaze interaction prefabs are used and work
  
  - GazeInteraction: Contains the Framework for the gaze interaction prefabs and the folder prefab contains the actually GazeInteraction prefabs.
    - In the prefabs folder there are two prefabs. 
    - The GazeInteractable prefab: This will be attached to a gameobject and this allows ojects to be interacted with
    - The GazeInteractor prefab: This will be attached to the player and allow them to interact with any object that has the GazeInteractable prefab attached.
  
  - Old Fabs: Is a folder that has the old revisions of the Tour Prefabs such as video interactor. This folder is still here because this is the orgin for the newer versions of theses prefabs and deleting one of them could make some prefabs not work properly
  
  - Tour Prefabs: This folder contains prefabs that are used for a specific purpose, such as video interactors or text interactors. Theses can be draged and droped into the scence and should work without to much set up.
    - Interactable Empty is a empty interactable area that makes areas or images    in the case of a photosphere interactable
    - Title Block is a UI(User Interface) that can act as a menu or title screen
    - Video Interactor is a interactable area that prompts the user to learn more by playing a video that is in the url field of the video play script
   
# My Scripts
    A folder that contains scripts for the interactable elements used for a specific purpose.
    
# PhotoSphere 
  A folder that contains assets and prefabs for creating  and forming photospheres
    - PhotoSpheres folder contains photos for the reptile lab apart of this demo.
    - Prefabs
      - The only prefab that is import in this folder is the psv4 prefab which is the photosphere prefab that will accept an image and then rap it around sphere evenly
      - Old folder is the original photosphere prefabs that are needed for the PSV4 prefab to work
      
# Player Controls
  A folder that cotains the player control scripts, input system plugins, and player and camera prefabs.
  
  The Starter Assets folder is the main folder that has all the player assets, settings, and prefabs that are used in this demo and that are needed. In this folder there is seperate documentation pdfs that explain the all the assets in the folder. The pdf is called StarterAssets_Documentation.
  
  Assets used in the project and are needed for player input are
  
    - PlayerCapsule prefab
    - PlayerFollowCamera prefab
    - UI_Canvas_StarterAssetsInputs_Joysticks prefab
    - UI_EventSystem prefab 
    - MainCamera prefab x2
    
# Streaming Assets
  The Video Render is placed in the second psv4 prefab under its Photo Gimbal componet. This used when video needs to be rendered instead of a photosphere. The video you want to play can then be attached to the video render. You cannot attach video directly to the psv4 asset. 
  
# Teleport System
  The teleport pad can teleport players in two ways. A coordinate transfer where the player transports to the coordinates specified in the script or a teleportation that transports them to a different scene.
  
  
# Sources and Future Considerations
  ## Video Streaming
