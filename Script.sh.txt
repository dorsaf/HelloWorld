#!/bash/bin
if [ "$#" -ne 1] 
then
echo " ERROR "
else 
exec &> Hello_$(date +%Y%m%d_%H%M).log
java -Xms512M -jar app-0.0.1-SNAPSHOT.jar $1
mv Hello_$(date +%Y%m%d_%H%M).log  /home/imid1/App/app/temps
fi