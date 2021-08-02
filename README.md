# pdfsign
Sign PDF (PAdES compatible)

Requirements:

PoDoFo (http://podofo.sourceforge.net/)

PKCS11 engine (https://github.com/opensignature/pkcs11engine)

OpenSSL ver. 3 (https://github.com/openssl/openssl)

Other standard library: (libjpeg, libfreetype, libz, libpthread, libfontconfig)


Compile with:

g++ pdfsign.cpp -I/usr/include/podofo/ -lpodofo -ljpeg -lfreetype -lpng -lz -lcrypto -lpthread -lfontconfig -o pdfsign


Execute with:

pdfsign -in infile.pdf -module modulepkcs11 -id idkey -pin pin

(*) modulepkcs11: 
is a library provided by the token provider like:
libbit4opki.so (Oberthur)
opensc-pkcs11.so (OpenSC)
libASEP11.so (Athena)
libeTPkcs11.so (SafeNet)
libsiecap11.so (Siemens)
