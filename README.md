# pdfsign
Sign PDF (PAdES compatible)

Requirements:

PoDoFo (http://podofo.sourceforge.net/)

OpenSSL ver. 3 (https://github.com/openssl/openssl)

Other standard library: (libjpeg, libfreetype, libz, libpthread, libfontconfig)


Compile with:

g++ pdfsign.cpp -I/usr/include/podofo/ -lpodofo -ljpeg -lfreetype -lpng -lz -lcrypto -lpthread -lfontconfig -o pdfsign


Execute with:

pdfsign -in infile.pdf -id idkey -cert certificate.pem

(*) extract idkey and certificate.pem with pkcs11-tool ( https://github.com/OpenSC/OpenSC )
