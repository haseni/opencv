# opencv
// ConsoleApplication1.cpp : 定义控制台应用程序的入口点。
//测试代码
#include "stdafx.h"
#include "cv.h"
#include <iostream>
#include <string>
#include "opencv2/imgproc/imgproc.hpp"
#include "opencv2/highgui/highgui.hpp"
using namespace cv;
using namespace std;

int _tmain(int argc, _TCHAR* argv[])
{
	string imagename="F:\\pig1.jpg";
	Mat gray_img=imread(imagename,0);
	Mat color_img=imread(imagename);

	if(color_img.empty())
	{
	cout<<"Could not open or find the image!"<<endl;
	return -1;
	
	}
	namedWindow("color_img",1);
	namedWindow("gray_img",1);

	imshow("color_img",color_img);
	imshow("gray_img",gray_img);

	waitKey(0);
	return 0;
}


