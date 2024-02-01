# Awesome Egocentric Pose
A list of awesome egocentric pose estimation works and related resources.

## Egocentric Inside-In Pose Estimation

The inside-in vision setup involves cameras or sensors directed toward the person or object of interest, capturing data from the inside of the motion capture subject. This setup can be seen on the Oculus Quest2 and Apple Vision Pro.


### Training Datasets

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
    <td class="tg-0lax">Mo2Cap2 <a href="#1">[1]</a></td>
    <td class="tg-0lax">530K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax"><a href="https://vcai.mpi-inf.mpg.de/projects/wxu/Mo2Cap2/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax">xR-egopose</td>
    <td class="tg-0lax">380K</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">46</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">30</td>
    <td class="tg-0lax"><a href="https://github.com/facebookresearch/xR-EgoPose">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax">EgoPW</td>
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
    <td class="tg-0lax">EgoWholeBody</td>
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
    <td class="tg-0lax">UnrealEgo</td>
    <td class="tg-0lax">450K * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">17</td>
    <td class="tg-0lax">No</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax"><a href="https://4dqv.mpi-inf.mpg.de/UnrealEgo/">Link</a></td>
  </tr>
  <tr>
    <td class="tg-0lax">UnrealEgo2</td>
    <td class="tg-0lax">1.25M * 2 views</td>
    <td class="tg-0lax">Synthetic</td>
    <td class="tg-0lax">17</td>
    <td class="tg-0lax">Yes</td>
    <td class="tg-0lax">25</td>
    <td class="tg-0lax">-</td>
  </tr>
</tbody>
</table>

### Evaluation Datasets

#### SceneEgo Test Dataset [[Paper with Code](https://paperswithcode.com/sota/egocentric-pose-estimation-on-sceneego)]

### Papers

<p id="1">[1] Weipeng Xu et al. “Mo2Cap2 : Real-time Mobile 3D Motion Capture with a Cap-mounted Fisheye Camera”. In: IEEE Transactions on Visualization and Computer Graphics (2019), pp. 1–1. issn: 1077-2626. doi: 10.1109/TVCG.2019.2898650.</p> 




## Egocentric Inside-Out Pose Estimation

The inside-out vision setup employs cameras or sensors positioned on the person or device, looking outward to the environment. This approach is commonly used in most virtual reality (VR) headsets and augmented reality (AR) systems, where cameras attached to the headset capture the user's surroundings and interpret motion relative to them. 

### Datasets

### Papers

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

## Mixed Setup

Combination of aforementioned setups.
