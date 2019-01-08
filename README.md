#include <stdio.h>
void wczytaj(double *a1, double *b1, double *c1, double *a2, double *b2, double *c2){
	puts("podaj wspolczynnik a1");
        scanf("%lf",a1);
        puts("podaj wspolczynnik b1");
        scanf("%lf",b1);
        puts("podaj wspolczynnik c1");
        scanf("%lf",c1);
        puts("podaj wspolczynnik a2");
        scanf("%lf",a2);
        puts("podaj wspolczynnik b2");
        scanf("%lf",b2);
        puts("podaj wspolczynnik c2");
	scanf("%lf",c2);
}
double wyznacznik_glowny(double a1,double b2,double b1,double a2)
{
return a1*b2-b1*a2;
}
double wyznacznik_x(double c1, double b2, double b1, double c2)
{
return c1*b2-b1*c2;
}	
double wyznacznik_y(double a1, double c2, double c1, double a2)
{
return a1*c2-c1*a2;
}
int main()
{
	double a1,b1,c1,a2,b2,c2,x,y;
	double W, Wx, Wy;
	wczytaj(&a1, &b1, &c1, &a2, &b2, &c2);
	W = wyznacznik_glowny(a1,b2,b1,a2);
	Wx = wyznacznik_x(c1,b2,b1,c2);
	Wy = wyznacznik_y(a1,c2,c1,a2);
	x=Wx/W;
	y=Wy/W;

	printf("x wynosi %lf, a y wynosi %lf",x,y);
	return 0;
}
