+package 记事本;
+import java.awt.*;
+import javax.swing.*;
+import java.awt.Event.*;
+public class L5_15记事本界面 extends JFrame
+{
+	JMenuBar cd;
+	JMenu cd1,cd2,cd3,cd4,cd5;
+	JMenuItem cdx2,cdx3,cdx4,cdx5,cdx6,cdx7;
+	JMenu ej;        JMenuItem ej1,ej2;
+	//JMenuItem  是最终的，不可以再有下一级菜单，而是直接出现应用效果。
+	//JMenu  不是最终的，点击以后不是应用效果，而是下一级菜单。
+	
+	
+	JToolBar gjt; // 工具条
+	JButton an1,an2,an3,an4,an5,an6;
+	
+	JTextArea wby;
+	JScrollPane gdt;
+	
+	
+	public static void main(String[] args)
+	{
+		L5_15记事本界面 AA=new L5_15记事本界面();
+	}
+	public L5_15记事本界面()
+	{
+		gjt=new JToolBar();
+		an1=new JButton(new ImageIcon("记事本图标/新建.png"));
+		an1.setToolTipText("新建");
+		an2=new JButton(new ImageIcon("记事本图标/打开.png"));
+		an2.setToolTipText("打开");
+		an3=new JButton(new ImageIcon("记事本图标/保存.png"));
+		an3.setToolTipText("保存");
+		an4=new JButton(new ImageIcon("记事本图标/剪切.png"));
+		an4.setToolTipText("剪切");
+		an5=new JButton(new ImageIcon("记事本图标/复制.png"));
+		an5.setToolTipText("复制");
+		an6=new JButton(new ImageIcon("记事本图标/粘贴.png"));
+		
+		
+		
+		cd=new JMenuBar();
+		cd1=new JMenu("文件(F)");
+		cd1.setMnemonic('F');
+		cd2=new JMenu("编辑(E)");
+		cd2.setMnemonic('E');
+		cd3=new JMenu("格式(O)");
+		cd3.setMnemonic('O');
+		cd4=new JMenu("查看(V)");
+		cd4.setMnemonic('V');
+		cd5=new JMenu("帮助(H)");
+		cd5.setMnemonic('H');
+		
+		
+		ej=new JMenu("新建");
+		ej1=new JMenuItem("文件",new ImageIcon("记事本图标/文件.png"));
+		ej2=new JMenuItem("模板");
+		
+		
+		cdx2=new JMenuItem("打开",new ImageIcon("记事本图标/打开.png"));
+		cdx3=new JMenuItem("保存(s)",new ImageIcon("记事本图标/保存.png"));
+		cdx3.setMnemonic('S');
+		cdx4=new JMenuItem("另存为");
+		cdx5=new JMenuItem("页面设置");
+		cdx6=new JMenuItem("打印");
+		cdx7=new JMenuItem("退出");
+		
+		wby=new JTextArea();
+		gdt=new JScrollPane(wby);
+		
+		
+		gjt.add(an1);  gjt.add(an2);  gjt.add(an3);
+		gjt.add(an4);  gjt.add(an5);  gjt.add(an6);
+		
+		ej.add(ej1);   ej.add(ej2);
+		
+		cd1.add(ej);   cd1.add(cdx2); cd1.add(cdx3);  cd1.add(cdx4);
+		cd1.addSeparator();
+		cd1.add(cdx5);   cd1.add(cdx6);
+		cd1.addSeparator();
+		cd1.add(cdx7);
+		
+		cd.add(cd1);   cd.add(cd2);    cd.add(cd3);
+		cd.add(cd4);   cd.add(cd5);
+		
+		
+		this.setJMenuBar(cd);
+		this.add(gjt,BorderLayout.NORTH);
+		this.add(gdt);
+		
+		ImageIcon	tp1=new ImageIcon("记事本图标/记事本.png");
+		this.setIconImage(tp1.getImage());
+		this.setTitle("记事本");
+		this.setSize(570,370);
+		this.setLocation(500,500);
+		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
+		this.setVisible(true);
+		
+	}
+}
