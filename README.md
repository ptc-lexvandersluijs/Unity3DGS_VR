# Unity3DGS_VR
This is my VR version of Aras' Toy 3D Gaussian Splatting project: https://github.com/aras-p/UnityGaussianSplatting. This repository contains a copy of the 'package' folder from the source project, in order to freeze it / make sure this project doesn't break when there are updates there.

The project includes 3 pre-made Gaussian Splats assets: Bicycle, Playroom and Bonsai. These are included for two reasons: a) these look good and perform well on the hardware used to test (NVidia RTX 3080 laptop), and b) the scene has been prepared for them, by rotating and scaling them to a pose that makes sense in VR, and by adding a floor with a collider for the user to walk on.

The Playroom (30k iterations) and Bonsai (7k iterations) datasets have Medium compression. The Bicycle (7k iterations) dataset has a custom compression, with quantized spherical harmonics, to fit the files within the 100 MB limit imposed by GitHub (without LFS).

It's easy to add more datasets to the scene: just use the GS Asset creation tool available in the menu. I used some 'reference cubes' to scale the splats point cloud to an approximately correct metric size.

Developed and tested with Unity 2023.1.14f1, and HTC Vive. Interaction profiles for other headsets have been added in the OpenXR settings, but not tested.

# Practical notes
- You need to manually enable the right GameObject "GaussianSplats [xxx]" before going to Play mode.
- I get best results when I minimize the Unity Editor (or close the Game panel) before putting on the headset.
- When I disabled Motion Smoothing  in the SteamVR settings -General tab- I had better results.

# TODO
- It would be great to have a menu in VR that allows switching between scenes.
- Some datasets could use some cleaning, using the tools that Aras recently added to this package.
- make the teleport interaction work more like in Valve's The Lab. Right now, the parabolic trajectory and target location are always visible.
   
# License
Same as the source project that I based this on, so MIT license.

# Contact
Lex van der Sluijs (lvandersluijs -youknowthedrill- ptc.com)
