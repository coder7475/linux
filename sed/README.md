# SED Command

**SED** = Stream EDitor

Given a text file named **file.txt**

```plaintext
// file.txt
Unix is a multitasking, multiuser operating system.
Unix development started in 1969 at Bell Labs
Linux is also based on Unix.
Unix is very powerful, Unix is very easy to learn.
```

## Replacing or Substituting pattern

replace 'Unix' with 'Linux'

```
sed 's/Unix/Linux/' file.txt
```

**Note**: above command will not make changes in the file and will only be displaying the changes on the console

## Reference

https://faun.pub/unix-sed-command-for-devops-professionals-70bea8bd21b8
