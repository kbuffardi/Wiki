# Clearing Disk Space in ECC Linux

ECC Linux has a small disk quota for students. Here are a few ways to clear disk space and to avoid using too much space.

### Identifying Space Usage

```sh
cd
du -s *
```
`du` is a simple command line tool that allows you to see what files are using the most space. It is mostly fine to remove object (.o) files or executable files.

### Clear the Cache

```sh
cd
rm -r .cache
```
### Archiving Files

If have completed a class but do not want to remove the files from ECC Linux, consider archiving the class folder.

```sh
tar -czf <NAME> <PATH>
```

You can then transfer the file to your home computer via an SFTP Client like Filezilla or Cyberduck

You can uncompress the archive with: 
```sh
tar -xvf <PATH>
```


### VSCode

Do **NOT** use VSCode with ECC Linux. This uses a large amount of space and can quickly eat up your disk quota.

If you have used VSCode with ECC Linux you can remove the ssh files by using the following command:

```sh
cd
rm -r .vscode-server
```
