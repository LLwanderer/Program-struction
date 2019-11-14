package Main;
import java.util.Random;
public class Suanshi {
	public int x;
	int y;
	int w;
	static Suanshi[] suanshis = new Suanshi[55];
	public Suanshi(int x2, int y2, int w2) {
		// TODO Auto-generated constructor stub
		x=x2;
		y=y2;
		w=w2;
	}
	public Suanshi() {
		// TODO Auto-generated constructor stub
	}
	static int randoms() {
		Random random = new Random();
		return ((int)random.nextInt(100));
	}
	void Generating(){
		x=randoms();
		y=randoms();
		w=randoms();
		w=(w%2==0?1:-1);
	}
	int panduan(int s) {
		if((x+(y*w))<0 || (x+(y*w)>100))
			return s-1;
		for(int j=1;j<s;j++) {
			if(x==suanshis[j].x && y==suanshis[j].y && w==suanshis[j].w) {
				return s-1;
			}
		}
		output(s);
		return s;
	}
	void output(int s) {
		suanshis[s] = new Suanshi(x,y,w);
		System.out.print(s + " : ");
		System.out.print(x + (w==1?" + ":" - ") + y + " = " + (x+y*w));
		if(s%5==0) 
			System.out.println("");
		else
			System.out.print(" ");
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int i;
		for(i=1;i<=50;i++) {
			Suanshi suanshi = new Suanshi(); 
			suanshi.Generating();
			 i=suanshi.panduan(i);
		}
	}

}
