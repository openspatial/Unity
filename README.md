# Nod Unity SDK
Nod Unity SDK verison 1.0.3

The current build of the Nod Unity SDK supports PC, iOS, and Android for Unity 4.x, and Mac for Unity 5.x.

Min sys requirements to operate, in all cases a device that supports Bluetooth LE is required:
PC: Windows 8.1
iOs: iOs 8
Android: 4.3
Mac: OSX 10.10

After importing the NodUnitySDK.unitypackage, navigate to Assets\Nod\Examples\Scenes\ and load the various scene files to see examples of how you can use our APIs.  

Example1_Pos6d: Shows you how to read the rotation from the ring and apply it to a GameObject in Unity, and also how to read the button state.
Example2_TouchToMove:  Shows you have to use Position 2D mode and Gestures.
(There is no example3)
Example4_MultipleRings: Shows you how you can read data from multiple rings at the same time.

You will need to have our windows service installed to run on windows.  You can find the service installer here:
https://github.com/openspatial/openspatial-windows/tree/master/Nod%20Installer

Android requires a Nod app installed on the system (And your ring to be paired through the app and not at the system level), sign up for a developer account through www.openspatial.net to get the app.

If you want to quickly apply rotation from the ring to your own GameObjects for your own projects you can drag/drop the "Example1.cs" script from Assets\Nod\Examples\Scripts\ onto it.

When writing your own apps you can pick and choose what data you want from each ring by subscribing to the various services you are interested in.
SubscribeToButton
SubscribeToPose6D
SubscribeToGesture
SubscribeToPosition2D

You probable want to subscribe only to services you will use to minimize bluetooth traffic.  If you just want button data from one ring and Pose6D data from another ring, instead of subscribing both rings to pose6d and buttons you can subscribe one to pse6D and the other to buttons so both rings arn't broadcasting data they do not need.