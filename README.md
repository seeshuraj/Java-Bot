package bot.project;
import java.util.Random;
import java.util.Scanner;
import java.time.LocalDateTime;
import java.awt.*;
import java.applet.*;
import javax.swing.*;
import java.awt.event.*;
import java.awt.Image;
import java.io.IOException;

class Main extends JFrame{

    JTextArea txt;
    JButton btn;
    JLabel lb;

    public Main() throws IOException {

        setLayout(new FlowLayout());

        txt=new JTextArea(10,30);
        add(txt);

        btn=new JButton("send");
        add(btn);

        lb=new JLabel("");
        add(lb);

        JLabel ax=new JLabel(new ImageIcon("C:\\Users\\HP\\Desktop\\bot.png") );
        add(ax);

        event e=new event();
        btn.addActionListener(e);

    }
    public class event implements ActionListener{

        @Override

        public void actionPerformed(ActionEvent e) {

            String msg=txt.getText();
            String[][] a ={{"hi","hey","hola","hello"},{"what's up","what doing","sup","wassup"},{"help","help me","please help me","report"},{"conatct me","call me","call","feedback"},{"love you","ly","lysm","my love"},{"show date","show time","date","time"},{""}};
            for(int i=0;i<=10000;i++){

                for(int j=0;j<4;j++) {

                    if (msg.equalsIgnoreCase(a[0][j])){

                        Random r=new Random();
                        String[] h={"hello buddy","holaaa","hiiii"};
                        int max=2,min=0;
                        int s1=r.nextInt(max-min)+min;
                        lb.setText("wiz:"+h[s1]);

                    }
                    else if(msg.equalsIgnoreCase(a[1][j])){

                        Random r=new Random();
                        String[] h={"Thinking what to do..","just going threw the updates","little busy with small works"};
                        int max=2,min=0;
                        int s1=r.nextInt(max-min)+min;
                        lb.setText("wiz:"+h[s1]);

                    }
                    else if(msg.equalsIgnoreCase(a[2][j])){

                        lb.setText("wiz:"+"Yeah please let us know your query.\nMail us:seeshu12@gmail.com \n");

                    }
                    else if(msg.equalsIgnoreCase(a[3][j])){

                        lb.setText("wiz:"+"Give a missed call to\n 7299955537\n We will get back to you soon\n ");

                    }
                    else if(msg.equalsIgnoreCase(a[4][j])){

                        Random r=new Random();
                        String[] h={"Love you too...have a great day ^_^ ","Yo buddy love you too","Have a fab day love you"};
                        int max=2,min=0;
                        int s1=r.nextInt(max-min)+min;
                        lb.setText("wiz:"+h[s1]);

                    }
                    else if (msg.equalsIgnoreCase(a[5][j])){

                        LocalDateTime myObj = LocalDateTime.now();
                        lb.setText("wiz:"+String.valueOf(myObj));

                    }
                    else if(msg.equalsIgnoreCase("thank you")){

                        lb.setText("wiz:"+"Thank you for using seeshu's bot!!");

                    }
                    else if (msg.equalsIgnoreCase("pickup lines")){

                        Random r=new Random();
                        String[] x={"i'm just reading you to get ready for my entire life","I’d never play hide and seek with you because someone like you is impossible to find","I am going to complain to Spotify about you not being this weeks hottest single."};
                        int max=2,min=0;
                        int s1=r.nextInt(max-min)+min;
                        lb.setText("wiz:"+x[s1]);

                    }
                    else if(msg.equalsIgnoreCase("jokes")){

                        Random r=new Random();
                        String[] x={"I dated an English teacher for a few months, but it didn't work out.\nShe didn't approve of my improper use of the colon","There's 26 letters in the English language, combined to make millions of words, which are used to make infinite sentences for any event imaginable. . .\nYet I see the same jokes posted every day."};
                        int max=1,min=0;
                        int s1=r.nextInt(max-min)+min;
                        lb.setText("wiz:"+x[s1]);

                    }
                }
            }
        }
    }

    public static void main(String[] args) throws IOException {

        Main s=new Main();

        s.getContentPane().setBackground(Color.LIGHT_GRAY);
        s.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        s.setSize(500,500);
        s.setVisible(true);

    }
}
