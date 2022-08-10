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
    - Video Interactor is a interactable area that prompts the user to learn more by playing a video that is in the url field of the video play script. 
    - 
 **Note the type of url that needs to be put into the video play script will be explained in the sources and future considerations section under video streaming.**
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
  The Telepad is the main asset used for teleporting and can be found in the teleport system folder under Tour Prefabs.
  The teleport pad can teleport players in two ways. A coordinate transfer where the player transports to the coordinates specified in the script
  
  
  ![image](https://user-images.githubusercontent.com/110831080/183956226-ce56ccad-fcdc-467b-b554-3c11eb57478f.png)

  
  or 
  
  a teleportation that transports them to a different scene.
  
  
  ![image](https://user-images.githubusercontent.com/110831080/183954333-ea03b7e1-1932-49fe-a72e-4414442a450f.png)
  
  There is also the orginal prefab folder which houses the orginal teleportation pad prefab that I modifed to make this teleport system. https://assetstore.unity.com/packages/tools/custom-teleporter-pad-script-20098

  
  
# Sources and Future Considerations
  ## Video Streaming
  - The video streaming utility that I have utlized in this project is github pages. Github allows you to create a respository and upload a video or videos to the repository under 25 MB. Then this repository can be hosted as a web page and the meta data can be streamed from the repository. You can vist here for a full tutorial on how to use github pages https://simmer.io/articles/adding-video-to-unity-webgl/
  - Youtube API: The other method that can stream video is excute calls to  the Youtube API to get meta data for a specific video you want. The only problem with this is that unity has restricted calls to the youtube api. Luckly someone has found a soultion to this by first hosting a app that will send a call request to youtube api and then unity can call the metadata from that app.  The app can be hosted for free on Heroku https://id.heroku.com. The github repository for the person who created this method can be found here https://github.com/iBicha/UnityYoutubePlayer
    - I have hosted an app that already does this that you can use https://nawcadwolf-labtour.herokuapp.com/. 
    - To call meta data from youtube copy the watch?v=qZzhXHqXM-g part from the youtube link and then add it to the end of the apps url https://nawcadwolf-labtour.herokuapp.com/watch?v=qZzhXHqXM-g
    - There is also a youtube player asset that I have found in the unity store, it is a paid asset, but from the preview it seems to work pretty well. it even has a photosphere 360 video demo as well https://assetstore.unity.com/packages/tools/video/youtube-video-player-youtube-api-29704#content
    ### Render Streaming
    - Render Streaming is a possiblity where we might not even need to stream video. Render Streaing allows a unity application to host its contents using a local web server and other applications can access that content by connecting the web server. This allows all the video data which is a least 50 Gb to be stored on one computer and can just be streamed to the other devices. You can learn more by visting https://github.com/Unity-Technologies/UnityRenderStreaming.
      - The only problem I found while using this is it works like a live stream. Where the app on the main machine were the web server is, can only stream what is happening on the main machine to the other connected users. Not where the other users can access the app itself.
  ## Hosting
      
