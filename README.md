# bin_to_pcd
kitti_velodyne_bin2pcd
the code is from a blog in csdn(https://blog.csdn.net/u012411498/article/details/80716794)
it's very helpful.


b="0"; for x in /home/miranda/pcl_test_2/infile/*.bin; do i=${x#*$b}; /home/miranda/pcl_test_2/bin2pcd --infile $x --outfile PCD_data/$i.pcd; done
 
#for x in your/input/data/*.bin  这是一个循环遍历所有的输入bin文件，每次将一个bin文件的绝对路径传给x
#do build/bin2pcd 是运行前面生成的bin2pcd文件，路径根据实际情况调整
#--infile 是输入文件，--outfile 是输出文件 
#i 是输出文件的名称，i=${x#*$b}是表示截取x中第一个“_”（下划线）后的字符串
