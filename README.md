# NAWCAD-WOLF-VR-TOURS

This is a demo that ibncludes assets scripts, photosheres, etc that can be used to create a Google Cardboard based tour more smoothly.


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

