KolorEyesIframeAPI
==================

Overview
--------

The Kolor Eyes Iframe API allows you to control an embeded Kolor Eyes player on your website using Javascript.

This API let you do basic actions on the player like play, pause, change the volume level, retrieve information about current playback and so on.

You can also set custom callbacks and event listeners that will execute in response to player events.

You'll find examples on how to use the Kolor Eyes Iframe API in this GitHub repository.

Requirements
------------

1. An account on Kolor's [360 video hosting platform](http://eyes.kolor.com/en/login). It is on beta stage for now, get in touch with us to get an access.
2. An uploaded 360 video on our 360 video hosting solution.
3. A browser that supports the HTML5 postMessage feature:

>* IE - 8.0 +
>* FireFox - 3.0 +
>* Chrome - 1.0 +
>* Safari - 4.0 +
>* Opera - 9.5 +

API methods
-----------

Assuming you have instanciated the Kolor Eyes Iframe API under *api* var name, there is a list of available methods.

To know how to start with the API, you should take a look to our first example.


**isConnected**

    api.isConnected() :boolean
Returns (*boolean*) true if API is connected to the iframe, false if not.

**getInstanceId**

    api.getInstanceId() :string
Returns (*string*) the instance id of the player API object.

**play**

    api.play() :void
Plays the video.

**pause**

    api.pause() :void
Pauses the video.

**togglePlayback**

    api.togglePlayback() :void
Switch between play and pause.

**stop**

    api.stop() :void
Stops the video.

**setVolume**

    api.setVolume(volume:number) :void
Sets the player volume. Volume is a float between 0 and 1.

**getVolume**

    api.getVolume() :number
Returns (*number*) the player current volume, a float between 0 and 1;

**setCurrentTime**

    api.setCurrentTime = function(time:number) :void
Sets the current playback time. Accepts a float value for time in seconds.

**getCurrentTime**

    api.getCurrentTime() :number
Returns (*number*) the current video playback time in seconds.

**getTotalTime**

    api.getTotalTime() :number
Returns (*number*) the video total time in seconds.

**getFovMin**

    api.getFovMin() :number
Returns (*number*) the minimal camera FOV value(Field Of View) in degrees.

**getFovMax**

    api.getFovMax() :number
Returns (*number*) the maximal camera FOV value (Field Of View) in degrees.

**getFov**

    api.getFov = function() :number
Returns (*number*) the current camera FOV value (Field Of View) in degrees.

**setFov**

    api.setFov(fov:number) :void
Sets the current camera FOV value (Field Of View) in degrees.

**getYaw**

    api.getYaw() :number
Returns (*number*) the current camera Yaw value in degrees.

**getPitch**

    api.getPitch() :number
Returns (*number*) the current camera Pitch value in degrees.

**lookAt**

    api.lookAt(yaw:number, pitch:number) :void
Sets camera Yaw and Pitch at the same time. Accepts Yaw and Pitch values in degrees.	

**getProjection**

    api.getProjection() :string
Returns (*string*) the current camera projection type

**setProjection**

    api.setProjection(projection:string)
Sets the current camera projection type.
Accepts a string.
Available projections are listed in KolorEyesIframeAPI.projections constant.

**isPlaying**

    api.isPlaying() :boolean
Returns (*boolean*) the playback status, true if it's playing, false if not.

**resizeTo**

    api.resizeTo(width:number, height:number) :void
Resizes the iframe to a given size.
Accepts width and height values in pixels.

**enableUI**

    api.enableUI = function(options:string|array) :void
Enable all or a part of the player UI.
Accepts a string or an array of UI parts, available UI parts are described in KolorEyesIframeAPI.UI constant.
If no options are passed in arguments, all the UI will be enabled.

**disableUI**

    api.disableUI = function(options:string|array) :void
Disable all or a part of the player UI.
Accepts a string or an array of UI parts, available UI parts are described in KolorEyesIframeAPI.UI constant.
If no options are passed in arguments, all the UI will be disabled.

**setTitle**

    api.setTitle(title:string) :void
Sets the video title that will be displayed in the player UI.
Accept a string as title.
	
**getUpdatedValues**

    api.getUpdatedValues() :object
Returns (*object*) the full updated object values from the player.
It contains currentTime, volume, totalTime, fovMin, fovMax, fov, yaw, pitch, projection, isPlaying.

