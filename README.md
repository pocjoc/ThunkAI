# ThunkAI
Code to connect AI with the thunkable platform

To use it, you must have an AI model that will recognize the images.
You can try to generate it using the teachable machine (https://teachablemachine.withgoogle.com/)

Once you have the model generate, you must configure the url to point to the model.

Configuration parameters:<br>
All configuration parameters are defined with a name, a colon and the values. 
To define it from the thunkable platform, you must use the block call PostMessage from Web_viewer component

Parameters list:<br>
  URL: URL base where the teachable machine model and metadata is
    Ex: URL:https://teachablemachine.withgoogle.com/models/YUoaPsjXu/
  Debug: boolean to indicate the web page to run in debug mode
    Ex: Debug:0
  AudioOn:To enable the audio in the user media
    Ex: AudioOn:0
  WxH: Canvas and video size. Width x Height
    Ex: WxH:760x1024
  TimeStable: Time which is considered a stable image (in milliseconds)
    Ex: TimeStable:500
  Init: to initialize the model and start the camera to begin the recognition
  	The camera index is the parameter to sent (normally 0 for rear camera and 1 for front camera)
    Ex: Init:0


 Receiving the response<br>
 To receive the response, you must use receive message block from Web_viewer component.

 Please refere to ExampleDesign.jpg and ExampleBlock.jpg for the thunkable program that connects with this component.


 NOTES:
 - Important to add a Camera in order to set the right permisions to allow the mobile to use the camera
 - The Web_viewer's URL must be secure (https) to use the user media, if not an error will appear and no camera will be enabled
