

## Generating a new SSH key and adding it to the ssh-agent
### Generating a new SSH key
Paste the text below, substituting in your GitHub email address.
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases". 
```
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
```

### Adding your SSH key to the ssh-agent
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

## Adding a new SSH key to your GitHub account
### Copy the SSH key to your clipboard.
sudo apt-get install xclip
\#Downloads and installs xclip. If you don't have `apt-get`, you might need to use another installer (like `yum`)
xclip -sel clip < ~/.ssh/id_rsa.pub
\#Copies the contents of the id_rsa.pub file to your clipboard

### in the web
In the upper-right corner of any page, click your profile photo, then click Settings.
Authentication keysIn the user settings sidebar, click SSH and GPG keys.
SSH Key buttonClick New SSH key or Add SSH key.
In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".
The key fieldPaste your key into the "Key" field.
The Add key buttonClick Add SSH key.
Sudo mode dialogIf prompted, confirm your GitHub password. 

## Testing your SSH connection
ssh -T git@github.com
\# Attempts to ssh to GitHub
## 参考
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
https://help.github.com/articles/testing-your-ssh-connection/

## 小结
完成以上步骤之后，就可以正常使用了。
