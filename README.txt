Implementasi Algoritma DDA

Dalam project ini menggunakan Aplikasi CodeBlock sebagai tempat penulisan codingnya.
agar dapat menjalankan Project ini Codeblocknya harus sudah di include glut.h di MINGW -nya.
untuk cara include glut.h dapat dilihat di video ini : https://youtu.be/pak-Z6uQjAQ.

Algoritma DDA adalah suatu algoritma yang digunakan menggambar garis. 
Garis yang dapat digamabar adalah garis vertikal,horisontal, atau miring 45 derajat.
Kelebihan Algoritma ini dapat menggambar garis ke segala arah dengan code yang sedikit 
dan logika yang mudah.
Tetapi Algorima ini mempunyai kelemahan yaitu menggunakan pembualatan sehingga kurang presisi. 

Project ini menggunakan user input dalam menentukan titik awal (x1,y1) dan titik Akhirnya (x2,y2),
dengan catatan semua nilai x1,y1,x2,y2 harus positif.

Output program ini berupa garis yang digambar di window baru dan panjangnya sesuai dengan input.

Algoritma DDA yang digunakan :


Int dx = x2-x1;
Int dy = y2-y1;
Int steps,k,x1,y1,x2,y2;
Float x_inc, y_inc;
Float x = x1;
Float y = y1;

If (abs(dx)>abs(dy)) 
	steps = abs(dx) 
else 
	steps = abs(dy);

X_inc = dx/(float)steps;
Y_inc = dy/(float)steps;

setPixel(Round(x),Round(y));

For(k=0;k<steps;k++) {
	x+=x_inc;
	y+=y_inc;
	setPixel(Round(x),Round(y));

}
