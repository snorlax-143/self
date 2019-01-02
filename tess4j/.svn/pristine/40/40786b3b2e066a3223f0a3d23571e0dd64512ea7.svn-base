package com.test.tess4j;

import java.io.File;
import java.io.FileWriter;
import java.io.IOException;
import java.util.UUID;

import net.sourceforge.tess4j.ITesseract;
import net.sourceforge.tess4j.Tesseract;
import net.sourceforge.tess4j.TesseractException;

public class Test2 {
	public static void main(String[] args) throws Exception {
		judgePic();
		
//		generateUUIDs(83405);
	}
	

	public static void judgePic() throws IOException {

    	String path = "C:\\Users\\19708\\Desktop\\test pic";		//我的项目存放路径
    	
    	File file = new File(path + "//3R]%7JRIR8~%]]%VQ9{P2RN.jpg");
        ITesseract instance = new Tesseract();
 
        /**
         *  获取项目根路径，例如： D:\IDEAWorkSpace\tess4J
         */
        File directory = new File(path);
        String courseFile = null;
        try {
            courseFile = directory.getCanonicalPath();
        } catch (IOException e) {
            e.printStackTrace();
        }
        
        //设置训练库的位置
        instance.setDatapath(courseFile + "//tessdata");
 
        instance.setLanguage("chi_sim");//chi_sim ：简体中文， eng	根据需求选择语言库
        String result = null;
        try {
            long startTime = System.currentTimeMillis();
             result =  instance.doOCR(file);
            long endTime = System.currentTimeMillis();
            System.out.println("Time is：" + (endTime - startTime) + " 毫秒");
        } catch (TesseractException e) {
            e.printStackTrace();
        }
        
        System.out.println("result: ");
        System.out.println(result);
	}
	
	public static void generateUUIDs(int number) throws IOException {
		FileWriter fileWriter = new FileWriter("C:\\Users\\19708\\Desktop\\test.txt");
		StringBuilder sb = new StringBuilder();
		for (int i = 0; i < number; i++) {
			sb.append(UUID.randomUUID())
				.append("\n");
		}
		fileWriter.write(sb.toString());
		fileWriter.close();
	}
}


 
