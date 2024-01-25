mkdir cs378
cd cs378

https://www.cs.utexas.edu/users/flame/laff/pfhp/week0-installing-BLIS.html

git clone git@github.com:flame/blis.git 

cd blis 

git checkout pfhp

./configure -t openmp -p ~/blis auto    
make -j8
make check -j8
make install


cd ..

git clone git@github.com:utcs378-pfcp/cs378pfcp-loopordering.git 

cd cs378pfcp-loopordering

make IJP


Implement GEMV as a loop around DOTS
Edit Dots.c
Edit Gemv_I_Dots.c 

To Run
make I_Dots 

Edit Axpy.c
Edit Gemv_J_Axpy.c
To run
make J_Axpy

Edit Ger_J_Axpy.c
To run
make Ger_J_Axpy

Edit Ger_I_Axpy.c
To run
make Ger_I_Axpy
