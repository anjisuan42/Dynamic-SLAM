

# Dynamic SLAM

SLAM in Dynamic Environments (SLAMIDE)











# 综述



的传统的动态环境下的SLAM方法可以分为两大类:

一类是动态目标的检测和跟踪[20];

二是检测动态对象并过滤[21]。

2018年，Bahraini等人[31]提出了一种分段跟踪多次移动的方法对象，使用MultiLevel-RANSAC。

M. S. Bahraini, M. Bozorg, and A. B. Rad, "SLAM in dynamic environments via ML-RANSAC," Mechatronics, vol. 49, pp. 105-118, 2018/02/01/
2018.

总的来说，大多数视觉研究者仍然关注于如何从图像中提取动态对象相邻帧采用特征检测方法。特征检测方法的一个潜在缺点是，当检测到动态对象移动太慢或太快。Muhamad等人[32]对视觉SLAM和结构问题进行了调查来自动态环境中的运动(SfM)。根据分类，



其挑战主要来自两个方面:

一是难以从平面像素定义动态对象;

第二，动态对象不容易检测和跟踪。



由于深度学习在目标检测方面取得了良好的性能，许多研究者将深度学习与目标检测相结合SLAMIDE问题[32]。Zhang等人[33]集成了深度CNN模型，提高了地形分割的精度让它在野外环境中更强壮。一些类似的RGB-D SLAMIDE研究[34-37]已经由将最先进的SLAM框架与深度学Y. Sun, M. Liu, and M. Q. H. Meng, "Motion removal for reliable RGB-D SLAM in dynamic environments," Robotics and Autonomous Systems, vol.
108, pp. 115-128, 2018/10/01/ 2018.
[35] C. Yu et al., "DS-SLAM: A Semantic Visual SLAM towards Dynamic Environments," presented at the 2018 IEEE International Conference on
Intelligent Robots and Systems (IROS), 2018.
[36] F. Zhong, S. Wang, Z. Zhang, C. Chen, and Y. Wang, "Detect-SLAM: Making Object Detection and SLAM Mutually Beneficial," in 2018 IEEE Winter
Conference on Applications of Computer Vision (WACV), 2018, pp. 1001-1010.
[37] R. Scona, M. Jaimez, Y. Petillot, M. Fallon, and D. Cremers, "StaticFusion: background reconstruction for dense RGB-D SLAM in dynamic
environments," presented at the 2018 IEEE International Conference on Robotics and Automation (ICRA), 2018.习网络相结合，取得了可观的成果。





大。Barnes等人[39]提出了一种自我监督的方法来忽略单目相机图像中的干扰物，使之具有鲁棒性城市动态环境中车辆运动的估计。

Bescos等人[40]对我们使用了类似的方法。他们的总和ORB-SLAM2与RCNN[41]掩模实现了动态环境下的单目与立体系统的结合多视图几何模型和深度学习算法实现RGB-D系统。



# 已阅读



## Dynamic-SLAM: Semantic monocular visual localization and mapping based on deep learning in dynamic environment-2019

肖等人[15]提出Dynamic-SLAM，构建基于卷积神经网络的SSD目标检测器，并提出基于相邻帧等速的漏检补偿算法，解决SSD目标检测网络召回率低的问题，大大提高检测的召回。还提出了一种选择性跟踪算法来简单地消除动态对象，从而提高了系统的鲁棒性和准确性





## Semantic SLAM Based on Improvement DeepLabv3+ in Dynamic Scenarios - 2022

为了消除动态物体对系统定位精度的影响，我们提出了DeepLabv3+_SLAM系统。该系统在原始 ORB-SLAM3 的基础上引入了语义和几何线程。首先，通过语义线程获得先验动态信息。然后，使用多视图几何方法在几何线程中检测场景中的动态特征点，同时提出一种新的蚁群策略，利用特征点的分布特征选择性地检测动态特征点，以便提高几何线程的实时性能。最后，为了验证本文系统的整体性能，我们在 TUM RGB-D 数据集上进行了实验和分析，结果表明本文系统的定位精度和实时性都有所提高。与现有的高级 SLAM 框架相比，在高度动态的环境中。

尽管在定位精度和实时性方面取得了进步，但仍然存在许多不足。一方面，系统的实时性仍有待提高，几何线程图像帧处理的速度有待提高。另一方面，我们仍然需要不断优化语义分割网络来提高网络分割的准确性，或者选择其他优秀的轻量级网络来帮助系统更有效地消除动态对象带来的影响。





# 等待阅读



[11] C. Yu, Z. Liu, X.-J.Liu, F. Xie, Y. Yang, Q. Wei, and Q. Fei, ‘‘DS-SLAM: A semantic visual SLAM towards dynamic environments,’’ in Proc.IEEE/RSJ Int.Conf.Intell.Robots Syst.(IROS), Oct. 2018, pp. 1168–1174.

于等人[11] 提出了一种 DS-SLAM 方案，将视觉 SLAM 算法与 SegNet [12] 网络相结合，利用动态场景中的语义信息和运动特征点来过滤动态部分。该方法提高了姿态估计的准确性，但该方案中语义分割网络能够识别的对象类型有限，限制了其应用范围。





[16] L. Cui and C. Ma, ‘‘SOF-SLAM: A semantic visual SLAM for dynamic environments,’’ IEEE Access, vol.7, pp. 166528–166539

Cui 和 Ma [16] 提出了一种语义光流方法，它结合了运动前的语义信息，辅助计算极线几何，过滤掉真正的动态特征，只保留剩余的静态特征进入跟踪优化模块，以实现在动态环境中准确估计相机位姿





[17] J. Zhang, M. Henein, R. Mahony, and V. Ila, ‘‘VDO-SLAM: A visual dynamic object-aware SLAM system,’’2020,arXiv:2005.11052.

张等人[17] 提出了 VDO-SLAM，一种基于动态特征的 SLAM 系统，它利用场景中基于图像的语义信息，无需事先了解物体姿态或几何形状，即可同时实现动态物体的定位、地图构建和跟踪。但是，也存在由于算法或优化功能的问题而出现较大误差的情况，实时性能需要改进。





[18] J. Cheng, Z. Wang, H. Zhou, L. Li, and J. Yao, ‘‘DM-SLAM: A feature- based SLAM system for rigid dynamic scenes,’’ ISPRS Int.J. Geo-Inf., vol.9, no.4, pp. 1–18, 2020.

陈等人[18] 提出了 DM-SLAM，它将实例分割网络 Mask-R CNN 与光流和对极几何相结合，以约束场景中的异常值。提出了两种不同的策略来获得动态点检测段中潜在动态对象的分割结果。一种方法是将具有深度信息的特征点重投影到当前帧，并使用重投影偏移向量来区分动态点。另一种方法使用极线几何约束。





[19] X. Long, W. Zhang, and B. Zhao, ''PSPNet-SLAM: A semantic SLAM detect dynamic object by pyramid scene parsing network,'' IEEE Access, vol.8, pp. 214685–214695, 2020.

龙等人[19]提出PSPNet-SLAM，通过金字塔场景分辨率SLAM将金字塔结构的语义线程和几何线程整合到ORB-SLAM2中，利用语义线程结合上下文信息对动态对象进行分割。最佳误差补偿单应矩阵旨在提高动态点检测的精度，但网络处理图像帧的能力影响系统的实时性，去除动态对象的能力有待提高。





[20] B. Bescos, J. M. Fácil, J. Civera, and J. Neira, ‘‘DynaSLAM: Tracking, mapping, and inpainting in dynamic scenes,’’ IEEE Robot.Automat.Lett., vol.3, no.4, pp. 4076–4083, Oct. 2018.

贝斯科斯等人[20] 提出了 DynaSLAM，它以不同的方式处理单目和 RGB-D 相机。在单目情况下，Mask R-CNN [21] 用于检测运动物体，而在 RGB-D 模式下，Mask R-CNN 网络和多视图几何模型相结合来检测运动物体。该方法可以检测环境中的多个运动物体，并修复被动态物体遮挡的背景。然而，该系统难以实时运行，因为 Mask R-CNN 网络在图像处理方面既费时又费资源。





[22] Y. Ai, T. Rui, M. Lu, L. Fu, S. Liu, and S. Wang, ''DDL-SLAM: A robust RGB-D SLAM in dynamic environments combined with deep learning,''IEEE Access, vol.8, pp. 162335–162342, 2020.

艾等人[22] 提出了 DDL-SLAM 系统，该系统提高了分割和背景恢复能力。通过结合语义分割和多视图几何算法过滤掉场景中的动态对象，静态场景图可以修复被移动对象遮挡的背景进行恢复，从而提高高动态环境下的定位精度。然而，实时性能仍然不足







F. Zhong, S. Wang, Z. Zhang, C. Chen, and Y. Wang, ``Detect-SLAM:

Making object detection and SLAM mutually benecial,'' in Proc. IEEE
Winter Conf. Appl. Comput. Vis. (WACV), Mar. 2018, pp. 10011010.

钟等人 [13]将ORB-SLAM2和SSD [14]组合成一个新的耦合框架Detect-SLAM，并提出了一种实时传播关键点运动概率的方法，以克服目标检测线程的延迟。语义信息用于消除 SLAM 中移动物体造成的负面影响。该框架旨在提高目标检测效率和对视点变换问题的敏感性，系统的实时性能有待进一步优化





# 存在问题

1.现在可以做RGBD-SLAM，也可以做Monocular-SLAM，到底做哪一个呢？两者的技术路线是有区别的

大部分的SLAM的研究人员将重点放在了激光雷达SLAM和RGB-D SLAM上，因为这些传感器可以直接获取深度信息估计动态对象[38]的位置。相比之下，对slam在单目视觉系统中的应用研究非常有限

Z. Lu, Z. Hu, and K. Uchimura, "Slam Estimation In Dynamic Outdoor Environments," International Journal of Humanoid Robotics, vol. 07, no. 02, pp.
315-330, 2010/06/01 2010.



2.哪怕是语义分割网络，也只能先验地检测出具有高概率的动态对象，但在实际场景中，SLAM 系统经常会受到静态对象的干扰。书籍和椅子是静态对象的示例。然而，当人带着书或椅子移动时，应将其视为动态物体，而不是将其视为静态物体参与定位和建图。

因此在检测的基础上，还需要加入动态物体和静态物体区分的部分，



将地图点云投影到当前帧，根据视点差异和深度值变化的大小，区分对象是动态对象还是静态对象。

视角变化值：

通过计算当前帧(cf)中每个关键点的视角值vcf和历史帧(hf)的视角值vhf，如果视角值的差大于设定阈值，确定关键点为动态点。

深度变化值：

同时，我们还需要计算当前帧中关键点的深度值dcf和当前帧中历史帧的投影深度值dproj。如果深度值之差为，则确定关键点为静态点。如果大于设置的阈值 dthresh，则认为关键点是动态的。

![image-20220420005625715](Dynamic%20SLAM.assets/image-20220420005625715.png)





# 关键点

1.速度

尽量基于CPU，不要使用GPU，能否做到20帧每秒

网络模型应该使用轻量级的模型

目前基于深度学习的语义SLAM，都忽略了SLAM的性能约束，虽然能够做到实时，但是很多情况下都是依靠较高的机器配置实现的

![image-20220420010007346](Dynamic%20SLAM.assets/image-20220420010007346.png)

2.提高剔除动态关键点的鲁棒性

RGB图像的检测框结果，可以传入深度图中，做简单的前背景剔除（OTSU阈值分割）经过测试发现不可行

可以添加目标级追踪，保证在暂时出现目标检测失败，没有检测框的情况下，系统的稳定性



3.特征点追踪，在相机移动速度很快的时，是会失效的，这是一个基于检测的动态SLAM很好的切入点



4.单目SLAM中，区分动态物体和未区分动态物体，其初始化成功率分别为75%和90%





# 语义分割的方法

1.OTSU阈值分割

2.kmeans聚类