# mods-theyAreBillions-EasyMode


The ZXRules.dat file is a password protected zip file containing the unit and building parameters.

The first step is to get the password of the file:
To do this, we use dnSpy (https://github.com/dnSpy/dnSpy ) and open Ionic.Zip.dll inside dnSpy.
Now we go to the Ionic.zip namespace and inside the ZipCrypto class, we put a breakpoint over the first line of the ForRead function.
Now, from Debug, we execute "Start debugging..." (F5) and as executable we choose TheyAreBillions.exe.

The execution will stop at the point of interruption and we must check that the value of the variable ZipEntry e is the one that corresponds to the file ZXRules.dat.
If it is not, we press continue until it is.
Once it is, we look at the value of the password variable and we already have the key of the zip file.

Now we can unzip the ZXRules.dat file with the key and edit anything we want.

To finish, it is necessary that the file be compressed again using zip and the same password.
