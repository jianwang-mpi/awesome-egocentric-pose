# Awesome Egocentric Human Pose

A list of the awesome egocentric human body pose estimation works and related resources. While some repositories [awesome-egocentric-vision](https://github.com/Sid2697/awesome-egocentric-vision) compile studies across the wide field of egocentric vision, none specifically focus on the niche area of egocentric human body pose estimation.

## Contents
We split this topic by different capture setups:

- [Egocentric Inside-In Pose Estimation](#egocentric-inside-in-pose-estimation)
- [Egocentric Inside-Out Pose Estimation](#egocentric-inside-out-pose-estimation)
- [IMU-Based Egocentric Pose Estimation](#imu-based-egocentric-pose-estimation)
- [Headset-Based Egocentric Pose Estimation](#headset-based-egocentric-pose-estimation)
- [Mixed Setup](#mixed-setup)


## Egocentric Inside-In Pose Estimation

The inside-in vision setup involves cameras or sensors directed toward the person or object of interest, capturing data from the inside of the motion capture subject. This setup can be seen on the Oculus Quest2 and Apple Vision Pro.


### Training Datasets (bold means recommended to use)

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">Setup</th>
    <th class="tg-0lax">Dataset</th>
    <th class="tg-0lax">Number of Frames</th>
    <th class="tg-0lax">Synthetic or Real</th>
    <th class="tg-0lax">Actor Number</th>
    <th class="tg-0lax">Scene Annotation</th>
    <th class="tg-0lax">FPS</th>
    <th class="tg-0lax">Link</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax" rowspan="5">Monocular Fisheye</td>
    <td class="tg-0lax">Mo2Cap2<a href="#inside_in_1">[2]</a></td>
    <td class="tg-0lax">530K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax"><a href="https://vcai.mpi-inf.mpg.de/projects/wxu/Mo2Cap2/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>xR-egopose</b><a href="#inside_in_2">[3]</a></td>
    <td class="tg-0lax">252K Train + 16 Val</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">34</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax"><a href="https://github.com/facebookresearch/xR-EgoPose">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>EgoPW</b></td>
    <td class="tg-0lax">318K</td>
    <td class="tg-0lax">Real (pseudo gt)</td>
    <td class="tg-0lax">10</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://people.mpi-inf.mpg.de/~jianwang/projects/egopw/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax">EgoPW-Scene</td>
    <td class="tg-0lax">92K</td>
    <td class="tg-0lax">Real (pseudo gt)</td>
    <td class="tg-0lax">10</td>
    <td class="tg-0lax">Pseudo Annotations</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://people.mpi-inf.mpg.de/~jianwang/projects/sceneego/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>EgoWholeBody</b></td>
    <td class="tg-0lax">700K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">14</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax">-</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="1">Stereo Perspecive<br></td>
    <td class="tg-0lax">EgoGlass</td>
    <td class="tg-0lax">172K</td>
    <td class="tg-0lax">Real</td>
    <td class="tg-0lax">10</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax">-</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="2">Stereo Fisheye<br></td>
    <td class="tg-0lax"><b>UnrealEgo</b></td>
    <td class="tg-0lax">450K * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">17</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://4dqv.mpi-inf.mpg.de/UnrealEgo/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>UnrealEgo2</b></td>
    <td class="tg-0lax">1.25M * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">17</td>
    <td class="tg-0lax">Yes</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax">-</td>
  </tr>
</tbody>
</table>

### Evaluation Datasets (bold means recommended to use)

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">Setup</th>
    <th class="tg-0lax">Dataset</th>
    <th class="tg-0lax">Number of Frames</th>
    <th class="tg-0lax">Synthetic or Real</th>
    <th class="tg-0lax">Scene Annotation</th>
    <th class="tg-0lax">FPS</th>
    <th class="tg-0lax">Link</th>
    <th class="tg-0lax">Leader Board</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax" rowspan="5">Monocular Fisheye</td>
    <td class="tg-0lax">Mo2Cap2</td>
    <td class="tg-0lax">5K</td>
    <td class="tg-0lax">Real</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://vcai.mpi-inf.mpg.de/projects/wxu/Mo2Cap2/">Link</a></td>
    <td class="tg-0lax">-</td>
  </tr>
 <tr>
    <td class="tg-0lax"><b>xR-egopose</b></td>
    <td class="tg-0lax">115K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax"><a href="https://github.com/facebookresearch/xR-EgoPose">Link</a></td>
    <td class="tg-0lax">-</td>
  </tr>
  <tr>
    <td class="tg-0lax">GlobalEgoMocap</td>
    <td class="tg-0lax">318K</td>
    <td class="tg-0lax">Real</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://people.mpi-inf.mpg.de/~jianwang/projects/globalegomocap/">Link</a></td>
        <td class="tg-0lax"><a href="https://paperswithcode.com/sota/egocentric-pose-estimation-on-globalegomocap">Paper With Code</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>SceneEgo</b></td>
    <td class="tg-0lax">28K</td>
    <td class="tg-0lax">Real</td>
    <td class="tg-0lax">Yes</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://people.mpi-inf.mpg.de/~jianwang/projects/sceneego/">Link</a></td>
    <td class="tg-0lax"><a href="https://paperswithcode.com/sota/egocentric-pose-estimation-on-sceneego">Paper With Code</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>EgoWholeBody</b></td>
    <td class="tg-0lax">133K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">-</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="3">Stereo Fisheye<br></td>
    <td class="tg-0lax"><b>UnrealEgo</b></td>
    <td class="tg-0lax">48K * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://4dqv.mpi-inf.mpg.de/UnrealEgo/">Link</a></td>
    <td class="tg-0lax"><a href="https://paperswithcode.com/sota/egocentric-pose-estimation-on-unrealego">Paper With Code</a></td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>UnrealEgo2</b></td>
    <td class="tg-0lax">123K * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">Yes</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">-</td>
  </tr>
  <tr>
    <td class="tg-0lax"><b>UnrealEgo2-RW</b></td>
    <td class="tg-0lax">130K * 2 views</td>
    <td class="tg-0lax">Real</td>
    <td class="tg-0lax">Yes</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">-</td>
  </tr>
</tbody>
</table>


### Papers
<a name="inside_in_1"></a>
1. Rhodin, Helge, et al. "[Egocap: egocentric marker-less motion capture with two fisheye cameras.](https://dl.acm.org/doi/pdf/10.1145/2980179.2980235?casa_token=_TJDPGqsnLgAAAAA:YmzArpjri1d2L5s-IlF_5a4ROjwfLOlSzhhhZMebks_FRQGB4ROPdmUA_fWl2O5z6P3wiEwk8CRyQQ)" ACM Transactions on Graphics (TOG) 35.6 (2016): 1-11. [[project page]](https://vcai.mpi-inf.mpg.de/projects/EgoCap/)
<a name="inside_in_2"></a>
2. Xu, Weipeng, et al. "[Mo2cap2: Real-time mobile 3d motion capture with a cap-mounted fisheye camera.](https://ieeexplore.ieee.org/iel7/2945/4359476/08643070.pdf?casa_token=e4SLB13uVgEAAAAA:2XRsNxwTMs6UIWZ4saiYNrL5sLPuSFB3Y8PPPQzxtkeTO8D8_yyMWlzLWeoYwbqk7PhF1YaWjtM)" IEEE transactions on visualization and computer graphics 25.5 (2019): 2093-2101. [[project page]](https://vcai.mpi-inf.mpg.de/projects/wxu/Mo2Cap2/content/mo2cap2.pdf)
<a name="inside_in_3"></a>
3. Tome, Denis, et al. "[xr-egopose: Egocentric 3d human pose from an hmd camera.](https://openaccess.thecvf.com/content_ICCV_2019/papers/Tome_xR-EgoPose_Egocentric_3D_Human_Pose_From_an_HMD_Camera_ICCV_2019_paper.pdf)" Proceedings of the IEEE/CVF International Conference on Computer Vision. 2019. [[dataset]](https://github.com/facebookresearch/xR-EgoPose)
<a name="inside_in_4"></a>
4. Zhang, Yahui, Shaodi You, and Theo Gevers. "[Automatic calibration of the fisheye camera for egocentric 3d human pose estimation from a single image.](https://openaccess.thecvf.com/content/WACV2021/papers/Zhang_Automatic_Calibration_of_the_Fisheye_Camera_for_Egocentric_3D_Human_WACV_2021_paper.pdf)" Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision. 2021.
<a name="inside_in_5"></a>
5. Wang, Jian, et al. "[Estimating egocentric 3d human pose in global space.](https://openaccess.thecvf.com/content/ICCV2021/papers/Wang_Estimating_Egocentric_3D_Human_Pose_in_Global_Space_ICCV_2021_paper.pdf)" Proceedings of the IEEE/CVF International Conference on Computer Vision. 2021. [[project page]](https://people.mpi-inf.mpg.de/~jianwang/projects/globalegomocap/) [[dataset]](https://people.mpi-inf.mpg.de/~jianwang/projects/globalegomocap/) [[demo]](https://people.mpi-inf.mpg.de/~jianwang/projects/globalegomocap/data/global_egomocap.mp4)
<a name="inside_in_6"></a>
6. Wang, Jian, et al. "[Estimating egocentric 3d human pose in the wild with external weak supervision.](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Estimating_Egocentric_3D_Human_Pose_in_the_Wild_With_External_CVPR_2022_paper.pdf)" Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2022. [[project page]](https://people.mpi-inf.mpg.de/~jianwang/projects/egopw/) [[dataset]](https://people.mpi-inf.mpg.de/~jianwang/projects/egopw/) [[demo]](https://people.mpi-inf.mpg.de/~jianwang/projects/egopw/data/camera_ready.mp4)
<a name="inside_in_7"></a>
7.  Akada, Hiroyasu, et al. "[UnrealEgo: A new dataset for robust egocentric 3d human motion capture.](https://arxiv.org/pdf/2208.01633)" European Conference on Computer Vision. Cham: Springer Nature Switzerland, 2022. [[project page]](https://4dqv.mpi-inf.mpg.de/UnrealEgo/) [[code]](https://github.com/hiroyasuakada/UnrealEgo) [[dataset]](https://4dqv.mpi-inf.mpg.de/UnrealEgo/) [[demo]](https://4dqv.mpi-inf.mpg.de/UnrealEgo/data/unrealego_distribution.mp4)
<a name="inside_in_8"></a>
8. Wang, Jian, et al. "[Scene-aware Egocentric 3D Human Pose Estimation.](https://people.mpi-inf.mpg.de/~jianwang/projects/sceneego/data/camera_ready.pdf)" Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2023. [[project page]](https://people.mpi-inf.mpg.de/~jianwang/projects/sceneego/) [[dataset]](https://people.mpi-inf.mpg.de/~jianwang/projects/sceneego/) [[code]](https://github.com/jianwang-mpi/SceneEgo)
<a name="inside_in_9"></a>
9. Park, Jinman, et al. "[Building Spatio-temporal Transformers for Egocentric 3D Pose Estimation.](https://arxiv.org/pdf/2206.04785)" arXiv preprint arXiv:2206.04785 (2022).
<a name="inside_in_10"></a>
10. Liu, Yuxuan, et al. "[EgoHMR: Egocentric Human Mesh Recovery via Hierarchical Latent Diffusion Model.](https://ieeexplore.ieee.org/iel7/10160211/10160212/10161247.pdf?casa_token=CiJvYD088esAAAAA:axYgjqN_RcSDA1TXNzgdO6pTmDvoLwVAT9jitPD-mrDIOOnlN_MH1m72eLgztegwHO6UtnAGfUo)" 2023 IEEE International Conference on Robotics and Automation (ICRA). IEEE, 2023.
<a name="inside_in_11"></a>
11. Wang, Jian, et al. "[Egocentric Whole-Body Motion Capture with FisheyeViT and Diffusion-Based Motion Refinement.](https://arxiv.org/pdf/2311.16495)" arXiv preprint arXiv:2311.16495 (2023).
<a name="inside_in_12"></a>
12. Akada, Hiroyasu, et al. "[3D Human Pose Perception from Egocentric Stereo Videos.](https://arxiv.org/abs/2401.00889)" arXiv preprint arXiv:2401.00889 (2023).

## Egocentric Inside-Out Pose Estimation

The inside-out vision setup employs cameras or sensors positioned on the person or device, looking outward to the environment. This approach is commonly used in most virtual reality (VR) headsets and augmented reality (AR) systems, where cameras attached to the headset capture the user's surroundings and interpret motion relative to them. 

### Datasets

### Papers

- [Ego-Body Pose Estimation via Ego-Head Pose Estimation](https://arxiv.org/pdf/2212.04636.pdf) - Jiaman Li · Karen Liu · Jiajun Wu. In CVPR 2023.

- [You2Me: Inferring Body Pose in Egocentric Video via First and Second Person Interactions](https://openaccess.thecvf.com/content_CVPR_2020/papers/Ng_You2Me_Inferring_Body_Pose_in_Egocentric_Video_via_First_and_CVPR_2020_paper.pdf) - Evonne Ng, Donglai Xiang, Hanbyul Joo, and Kristen Grauman. In CVPR 2020. [[demo]](http://vision.cs.utexas.edu/projects/you2me/demo.mp4) [[project page]](http://vision.cs.utexas.edu/projects/you2me/) [[dataset]](https://github.com/facebookresearch/you2me/tree/master/data#) [[code]](https://github.com/facebookresearch/you2me#)
  
- [Ego-Pose Estimation and Forecasting as Real-Time PD Control](https://openaccess.thecvf.com/content_ICCV_2019/papers/Yuan_Ego-Pose_Estimation_and_Forecasting_As_Real-Time_PD_Control_ICCV_2019_paper.pdf) - Ye Yuan and Kris Kitani. In ICCV 2019. [[code]](https://github.com/Khrylx/EgoPose) [[project page]](https://www.ye-yuan.com/ego-pose) [[demo]](https://youtu.be/968IIDZeWE0)
  
- [Seeing Invisible Poses: Estimating 3D Body Pose from Egocentric Video](https://openaccess.thecvf.com/content_cvpr_2017/papers/Jiang_Seeing_Invisible_Poses_CVPR_2017_paper.pdf) - Hao Jiang and Kristen Grauman. In CVPR 2017.

## IMU-Based Egocentric Pose Estimation

The Inertial Measurement Unit (IMU) setup utilizes sensors typically composed of accelerometers, gyroscopes, and sometimes magnetometers. In egocentric motion capture, IMUs are placed on the human body to capture dynamic motion and limb orientation changes. 

### Datasets

### Papers

## Headset-Based Egocentric Pose Estimation

Some methods use the headset 6dof pose (head pose) and VR controller 6dof pose (hand pose) to estimate full body pose. The hand and head poses come from the headset SLAM and VR controller, the input signal is much less noisy than the IMU setup. 

### Datasets

### Papers

## Third-Person View Egocentric Pose Estimation

The third-person setup refers to motion capture techniques that involve a third person carrying moving cameras observing the motion capture subject.

### Datasets

### Papers

- [EgoBody: Human Body Shape and Motion of Interacting People from Head-Mounted Devices](https://arxiv.org/pdf/2112.07642.pdf) - Siwei Zhang, Qianli Ma, Yan Zhang, Zhiyin Qian, Taein Kwon, Marc Pollefeys, Federica Bogo, Siyu Tang. In ECCV 2022. [[project page]](https://sanweiliti.github.io/egobody/egobody.html) [[dataset]](https://egobody.inf.ethz.ch/) [[code]](https://github.com/sanweiliti/EgoBody)

## Mixed Setup

Combination of aforementioned setups.
