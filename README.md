# RP24-DectionMode-Temp  

此文档还在填坑中，打完分区赛再继续完善

---

为促进新队伍视觉技术快速成长，老队伍不再固步自封，现开源RobotPilots视觉自瞄网络模型  

该模型的识别能力较强，能够缩小与强队之间的视觉识别GAP

---
backbone网络采用MobieNetV3，使用Openvino GPU推理，帧率可稳定125FPS（NUC12,实测NUC13更快，且NUC13更便宜)

Openvino代码仅供参考，不一定能跑（老东西已无力维护）

输出：0到8是四个关键点，顺序从左上角开始逆时针；9到13是颜色（红蓝灰紫），13到22是数字

G（哨兵）
1（一号）
2（二号）	
3（三号）	
4（四号）	
5（五号）	
O（前哨站）
Bs（基地）
Bb（基地大装甲）	

---
使用指南：  

1、海康相机低曝光、高增益，光圈最大处往下拧一点  

2、烧饼使用模型时建议把置信度调高，避免误识别  

3、误识别一般只是闪过一帧，自瞄有连续三帧识别才锁敌的话问题不大   

4、步兵不要开异步推理

---

2024南部分区赛深圳大学VS哈尔滨工业大学（深圳）效果视频：  

链接：https://pan.baidu.com/s/1hkM0rZQneXRZiHC24oldig?pwd=RP24
提取码：RP24    
