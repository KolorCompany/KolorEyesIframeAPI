KolorEyesIframeAPI
==================

Important note!
--------

Kolor Eyes hosting in now [GoProVR](https://vr.gopro.com). (since 2016-04-18)
If you where an IframeAPI user previous to 2016-04-18, you may have some change to apply to your to make it work!

1/ All you iframe video url should begin by https://vr.gopro.com

2/ Same thing for the script who loads the iframeAPI the url is now : 
https://vr.gopro.com/API/KolorEyesPlayer/current/KolorEyesIframeAPI.min.js

Take a look at the updated example! Have fun!


Overview
--------

The Kolor Eyes Iframe API allows you to control a Kolor Eyes player in an iFrame embedded on your website, using Javascript.

This API lets you do basic actions on the player like play, pause, change the volume level, retrieve information about current playback and so on.

You can also set custom callbacks and event listeners that will execute in response to player events.

You'll find examples on how to use the Kolor Eyes Iframe API in this GitHub repository.

Requirements
------------

1. An account on GoProVR [360 video hosting platform](https://vr.gopro.com/). 
2. An uploaded 360 video on our 360 video hosting solution.
3. A browser that supports the HTML5 postMessage feature:

>* IE - 8.0 +
>* FireFox - 3.0 +
>* Chrome - 1.0 +
>* Safari - 4.0 +
>* Opera - 9.5 +

API methods
-----------

To know how to start with the API, you should take a look at our first example.

Assuming you have instantiated the Kolor Eyes Iframe API under *api* var name, there is a list of available methods and their signatures.

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
Returns (*number*) the current camera Yaw value in degrees. Yaw is the rotation of the camera around the horizontal axis, its value is between -180 and +180 degrees.

**setYaw**

    api.setYaw(yaw:number) :void
Sets the current camera Yaw value in degrees. Yaw is the rotation of the camera around the horizontal axis, its value is between -180 and +180 degrees.

**getPitch**

    api.getPitch() :number
Returns (*number*) the current camera Pitch value in degrees. Pitch is the rotation of the camera around the vertical axis, its value is between -90 and +90 degrees.

**setPitch**

    api.setPitch(pitch:number) :void
Sets the current camera Pitch value in degrees. Pitch is the rotation of the camera around the vertical axis, its value is between -90 and +90 degrees.

**lookAt**

    api.lookAt(yaw:number, pitch:number) :void
Sets camera Yaw and Pitch at the same time. Accepts Yaw and Pitch values in degrees.
Yaw is the rotation of the camera around the horizontal axis, its value is between -180 and +180 degrees.
Pitch is the rotation of the camera around the vertical axis, its value is between -90 and +90 degrees.	

**getProjection**

    api.getProjection() :string
Returns (*string*) the current camera projection type

**setProjection**

    api.setProjection(projection:string)
Sets the current camera projection type.
Accepts a string.
Available projections are listed in KolorEyesIframeAPI.projections constant.

**getVideoQualityCount**
    
    api.getVideoQualityCount() :number
Returns (*number*) the count of quality streams available for the video.

**getVideoQuality**

    api.getVideoQuality() :number
Returns (*number*) the current index of video quality (starts at 0).

**setVideoQuality**

    api.setVideoQuality(index:number)
Sets the current video quality index if it's available.

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

**showUI**

    api.showUI() :void
Shows the UI if it was previously hidden by hideUI.

**hideUI**

    api.hideUI() :void
Hides the UI.

**toggleShowSource**
    
    api.toggleShowSource() :void
Toggles the display of the bottom source view. This feature is only available when using the HTML5 player.

**showSource**
    
    api.showSource() :void
Shows the bottom source view. This feature is only available when using the HTML5 player.

**hideSource**
    
    api.hideSource() :void
Hides the bottom source view. This feature is only available when using the HTML5 player.

**setTitle**

    api.setTitle(title:string) :void
Sets the video title that will be displayed in the player UI.
Accept a string as title.

**setVelocity**

    api.setVelocity(velocity:number) :void
Sets the mouse velocity or sensitivity if you want to have a slower mouse velocity than the original value.
Default value is set to 10. It is not recommended to set an higher value than the default one, most people aren't hardcore gamers :)

**getUpdatedValues**

    api.getUpdatedValues() :object
Returns (*object*) the full updated object values from the player.
It contains currentTime, volume, totalTime, fovMin, fovMax, fov, yaw, pitch, projection, isPlaying.

**setUpdateRate**

    api.setUpdateRate(rate:number) :void
Sets the update rate of values for getters function in milliseconds.
The default rate is 100ms.

**getPlayerCoreType**

    api.getPlayerCoreType() :string
Returns (*string*) the player core type, it can be either "webgl" or "flash".
These values are listed in the constant KolorEyesIframeAPI.coreTypes

**kill**

    api.kill() :void
Kills the connection of the Iframe API


Events
------

The KolorEyes iframe API lets you listen to some player events and specify handling functions in response to these events.

Two methods are available to work with events.

Events type are listed in the KolorEyesIframeAPI.events constant.

In every handler function you will receive an event object in the first parameter with usefull data like a reference to the API.


## Method A

The easiest and the most common way to deal with events on Javascript : a single callback function for each event.
You can pass your handling functions on the 'events' object at the instanciation time, like on the first code exemple of this repository, or you can override handlers at the runtime, defining new functions for specific events.

**onReady**

    api.onReady()
This event is fired when the 360 player is ready, this is the best entry point for you to place your initialization code.

**onConnected**

    api.onConnected()
This event is fired when the API is connected to the Iframe. 

**onPlay**

    api.onPlay()
This event is fired when the video starts playing.

**onPause**

    api.onPause()
This event is fired when the user pauses the video playback.

**onVolumeChange**

    api.onVolumeChange()
This event is fired when the volume changes.

**onEnded**

    api.onEnded()
This event is fired when the video ends.

**onLoadedMetaData**

    api.onLoadedMetaData()
This event is fired when the meta date is loaded.

**onProjectionChange**

    api.onProjectionChange()
This event is fired when the camera projection changes.

**onSeek**

    api.onSeek()
This event is fired when the users seek through the video.

**onDisplaySourceChanged**
 
    api.onDisplaySourceChanged()
This event notifies you that the user display or hide the source view (available only in webGL)

**onValuesUpdated**

    api.onValuesUpdated()
This event is fired every time the api send the updated values


## Method B

The second method is made of event listeners. You can add and remove event listeners at the runtime.
This way you can bind multiple handlers for a single event type.

To function are available to this :

**addEventListener**

    api.addEventListener(eventType:string, handlerFunction:function) :void
Add an event listener for a given type of event. 
The handler function will be executed when the event type occured.
All event types are listed on the static variable : KolorEyesIframeAPI.events

**removeEventListener**

    api.removeEventListener(eventType:string, handlerFunction:function) :void
Remove an event listener for a given event type / handler. 

The event types are stored in KolorEyesIframeAPI.events constant 

    KolorEyesIframeAPI.events.ON_CONNECTED
    KolorEyesIframeAPI.events.ON_READY
    KolorEyesIframeAPI.events.ON_PLAY
    KolorEyesIframeAPI.events.ON_PAUSE
    KolorEyesIframeAPI.events.ON_VOLUME_CHANGE
    KolorEyesIframeAPI.events.ON_ENDED
    KolorEyesIframeAPI.events.ON_LOADED_META_DATA
    KolorEyesIframeAPI.events.ON_PROJECTION_CHANGE
    KolorEyesIframeAPI.events.ON_SEEK
    KolorEyesIframeAPI.events.ON_VALUES_UPDATED
    KolorEyesIframeAPI.events.ON_DISPLAY_SOURCE_CHANGED
    KolorEyesIframeAPI.events.ON_VIDEO_QUALITY_CHANGED

Release note
------------

## 1.1.0.400

- Added the onReady event that notifies you when the player is ready, this is the best entry point to begin !

- Added the onVideoQualityChanged event to know when the user change the quality stream index.

- Added a method to get the number of quality streams available for the current video : getVideoQualityCount

- Added a method to get and set the current quality index to play : getVideoQuality / setVideoQuality 

- Added a method to get the player core type (webgl or flash) : getPlayerCoreType

- Added a method kill() to kill the connection of the Iframe API

- Updated the example to demonstrate some of new features

## 1.0.0.400

- Added compatibility for https

## 1.0.0.106

- Added the onDisplaySourceChanged event that notifies you when the user displays or hides the source view ( KolorEyesIframeAPI.events.ON_DISPLAY_SOURCE_CHANGED )

- Updated the demo for the Kolor Eyes Hosting beta v2.

## 1.0.0.105

- Added the onValuesUpdated event ( KolorEyesIframeAPI.events.ON_VALUES_UPDATED )

- Added the setUpdateRate method 

## 1.0.0.104

- Bug fixed of the wrong values retuned by getter due to the asynchronous API.
Now you can get a value, set another new value and re-get the value. It's up to date.

- Bug fixed of the onLoadedMetaData event randomly fired.

- Added of some new methods to display the source bottom view (toogleShowSource, showSource, hideSource)

## 1.0.0.103

- Added a new method to set the velocity of the camera.

- Added new methods to show or hide the UI (showUI, hideUI).

- Improved compatibility with IE



