# ThunkAI
Code to connect AI with the thunkable platform

To use it, you must have an AI model that will recognize the images.
You can try to generate it using the teachable machine (https://teachablemachine.withgoogle.com/)

Once you have the model generate, you must configure the url to point to the model.

Configuration parameters:<br>
All configuration parameters are defined with a name, a colon and the values. 
To define it from the thunkable platform, you must use the block call PostMessage from Web_viewer component

Parameters list:<br>
  URL: URL base where the teachable machine model and metadata is<br>
    Ex: URL:https://teachablemachine.withgoogle.com/models/YUoaPsjXu/<br>
  Debug: boolean to indicate the web page to run in debug mode<br>
    Ex: Debug:0<br>
  AudioOn:To enable the audio in the user media<br>
    Ex: AudioOn:0<br>
  WxH: Canvas and video size. Width x Height<br>
    Ex: WxH:760x1024<br>
  TimeStable: Time which is considered a stable image (in milliseconds)<br>
    Ex: TimeStable:500<br>
  Init: to initialize the model and start the camera to begin the recognition<br>
  	The camera index is the parameter to sent (normally 0 for rear camera and 1 for front camera)<br>
    Ex: Init:0<br>


 Receiving the response<br>
 To receive the response, you must use receive message block from Web_viewer component.

 In the following images, you can see an example of a thunkable program that connects with this component.
 
<img src="https://github.com/pocjoc/ThunkAI/blob/main/ExampleDesign.jpg" />
<img src="https://github.com/pocjoc/ThunkAI/blob/main/ExampleBlocks.jpg" />

 Example<br>
 You can use an example of this page in the following URL:
 https://www.massabo.com/TechableMachine/TTM.html

 NOTES:
 - Important to add a Camera in order to set the right permisions to allow the mobile to use the camera
 - The Web_viewer's URL must be secure (https) to use the user media, if not an error will appear and no camera will be enabled
 - The Web_viewer component must have, ina advanced properties, 'AllowsInLineMediaPlayback' enabled and 'MediaPlaybackRequiresUserAction' disabled, as can be seen in the following image:
 <img src="https://user-images.githubusercontent.com/25144196/114837173-b711f600-9dd3-11eb-808e-0a1280e188a3.png" />


If you need some other resource, please feel free to contact me
