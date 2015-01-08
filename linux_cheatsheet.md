mkdir -p a/b/c
rmdir -p a/b/c

cd
cd -
cd ~user_dir

cp -r src dest
rsync -a src dest
cp -a src dest    (preserves attributes)

cat file1 file2
less file1 file2
head -n 10 file1
tail -n 10 file1

ln -s src dest
mv src dest
rmdir dir
rm -rf dir
file file1

ls -l
-a   (with attributes)
-t    (newest first)\
-S   (biggest first)
-r    (reversed order)

r(4) w(2) x(1)
u g o a
chmod u+w file
chmod g-r file
chmod o-x file
chmod a+rw file
chmod -R a+rX dir

grep what file
-i    (no case match)
-v   (not matching)
-r    (recursive)

sort file1

diff file1 file2
vimdiff file1 file2
tkdiff file1 file2
kompare file1 file2
meld file1 file2

ps axfj    process tree
pstree
top

du -chs file1 file2
df -h
df -i
wc file1   newlines/word/chars

du -chs file1 file2
df -h
df -i
wc file1   newlines/word/chars

tar -czf file.tgz   gzip
tar -cjf file.tar.bz2   bzip
tar xf file

zip -r arch.zip <files>
unzip arch.zip

who
whoami
id account
su -- account
su -- account -s /bin/bash
su account -c <commnand>

date
date +%F    2015-01-07

time command

date -s "2015-01-07 19:28:00"
rdate -s ntp.task.gda.pl

hwclock -systohc
hwclock -w

bc -l    float calculator
python
hex(80)

useradd -m user
shutdown -r now


