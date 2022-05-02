# LHL-Final-Project
Using generated 2d faces to create 3d models ready to deploy in unreal engine for game/cgi development.
Collab notebook for 3d face reconstruction is here: https://colab.research.google.com/drive/1LegDlY_PKTKYPmDzINH33Dg2RY4mg-Ri


## Code and pretrained models used from sources:
for StyleGAN2 pretrained model:\
[StyleGAN2](https://github.com/NVlabs/stylegan2)   Used stylegan2-ffhq-config-f.pkl pretrained model.\
https://github.com/AmarSaini/Epoching_StyleGan2_Setup   For custom latent traversal gifs.\
[align_face.py](https://gist.github.com/lzhbrian/bde87ab23b499dd02ba4f588258f57d5)\
[stylegan2directions](https://twitter.com/robertluxemburg/status/1207087801344372736)   Latent directions for traversing latent space.\
[stylegan2encoder](https://github.com/rolux/stylegan2encoder) Used to create images for later model, better than baseline projector\


\
For Deep3DFace Reconstruction pretrained model:\
[Deep3DFace Reconstruction](https://github.com/microsoft/Deep3DFaceReconstruction)   Microsoft face reconstruction from single image.\
[Basel Face Model 2009(BFM09)](https://faces.dmi.unibas.ch/bfm/main.php?nav=1-0&id=basel_face_model)\
[Expression Basis (transferred from Facewarehouse by Guo et al.)](https://github.com/Juyong/3DFace)   The original BFM09 model does not handle expression variations so extra expression basis are needed.\
[tf mesh renderer](https://github.com/google/tf_mesh_renderer/tree/ba27ea1798f6ee8d03ddbc52f42ab4241f9328bb)   This library is optionally used to render reconstruction images. Note that the rendering tool can only be used on Linux.
https://colab.research.google.com/drive/1oWjgftAf6e_yWvgZoXPLhF0UldfHg_Bt Using an edited version of this colab for generating the 3d face meshes. Materials are also created in a .mat file along with the mesh .obj file, but .mat is specific to 3DS Max while I'm using Blender for rendering the output. If you have 3DS MAX then knock yourselves out; it's apparently very easy to upload to a project.

You will need to aquire a few files (including align_face
