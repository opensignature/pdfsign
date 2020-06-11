# pdfsign
Sign PDF (PAdES compatible)

Requirements:

PoDoFo (http://podofo.sourceforge.net/)

PKCS11 engine (https://github.com/opensignature/pkcs11engine)

OpenSSL ver. 3 (https://github.com/openssl/openssl)

Other standard library: (libjpeg, libfreetype, libz, libpthread, libfontconfig)


Compile with:

g++ pdfsign.cpp -lpodofo -ljpeg -lfreetype -lpng -lz -lcrypto -lpthread -lfontconfig


Execute with:

pdfsign -in infile.pdf -module modulepkcs11 -id idkey -pin pin
