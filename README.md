# Menggunakan-Command-Help-di-Linux
Untuk mempelajari command apa pun, selalu disarankan untuk memulai dengan syntax command. Berikut adalah syntax untuk menggunakan command help:

help [options] [pattern]

⦁ [options] digunakan untuk mengubah perilaku default command help dengan menggunakan berbagai opsi yang tersedia.
⦁ [pattern adalah topik yang ingin di cari bantuannya. Dengan kata lain, di sinilah kita menentukan nama command yang diinginkan.

<h3>Mendapatkan bantuan dari command help itu sendiri</h3>
Ini akan menunjukkan apa yang seharusnya Anda harapkan dari command help:

```
help help
```
```
nyctoselene@Nyctoselene:~$ help help
help: help [-dms] [pattern ...]
    Display information about builtin commands.

    Displays brief summaries of builtin commands.  If PATTERN is
    specified, gives detailed help on all commands matching PATTERN,
    otherwise the list of help topics is printed.

    Options:
      -d        output short description for each topic
      -m        display usage in pseudo-manpage format
      -s        output only a short usage synopsis for each topic matching
                PATTERN

    Arguments:
      PATTERN   Pattern specifying a help topic

    Exit Status:
    Returns success unless PATTERN is not found or an invalid option is given.
nyctoselene@Nyctoselene:~$

```
Setelah Anda menjalankan command help, ia akan menampilkan deskripsi singkat command yang ditentukan beserta opsi yang tersedia.

<h3>Mendapatkan informasi command dalam man page</h3>
Man page memberikan deskripsi command, deskripsi opsi, dan lainnya.

Untuk menggunakan command help untuk mendapatkan informasi dalam format man page, gunakan syntax berikut:
```
help <nama_command>
```
Misalnya, kita akan mencari bantuan tentang command cd:
```
help cd
```
```
nyctoselene@Nyctoselene:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.

    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.

    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.

    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.

    Options:
      -L        force symbolic links to be followed: resolve symbolic
                links in DIR after processing instances of `..'
      -P        use the physical directory structure without following
                symbolic links: resolve symbolic links in DIR before
                processing instances of `..'
      -e        if the -P option is supplied, and the current working
                directory cannot be determined successfully, exit with
                a non-zero status
      -@        on systems that support it, present a file with extended
                attributes as a directory containing the file attributes

    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.

    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
nyctoselene@Nyctoselene:~$

```
mendapatkan bantuan dari command help di Linux
<h3>Mendapatkan deskripsi singkat tentang command</h3>
Untuk mendapatkan deskripsi singkat tentang command dengan command help, gunakan opsi `-d` sebagai berikut:

help -d <nama_command>
Misalnya, kita ingin mendapatkan deskripsi singkat tentang command cd lagi, maka gunakan command berikut:
```
help -d cd
```
```
nyctoselene@Nyctoselene:~$ help -d cd
cd - Change the shell working directory.
nyctoselene@Nyctoselene:~$
```
<h3>Mendapatkan syntax dari sebuah command</h3>
Kita juga dapat menggunakan command help untuk hanya mendapatkan syntax command tertentu. Untuk itu, kita harus menggunakan flag `-s` dengan cara berikut:

```
help -s <nama_command>
```
Berikut adalah cara mendapatkan syntax command cd menggunakan command help:
```
help -s cd
```
```
nyctoselene@Nyctoselene:~$ help -s cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
nyctoselene@Nyctoselene:~$
```

Sekian yang dapat saya sampaikan, mohon maaf apabila ada salah kata atau kekurangan dalam penyampaian. Akhir kata, Wassalam
