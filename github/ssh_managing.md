# To check ssh-key signature from github.com
```bash
ssh-keygen -E sha256 -l -f ~/.ssh/<key>.pub
```
## Establishing a connection...

# Possibly create a rsa_key
```bash
ssh-keygen -t rsa -C "admin@example.com"
```
## Copy the contents of id_rsa.pub to the github page for ssh keys...

# Test the connection
```bash
ssh -T git@github.com
```
#> It should not give any shell, but it should recognize you.

# Make sure your local git knows you...
```bash
git config --global -l
```
#if not
```bash
git config --global user.name your-name
  
git config --global user.email your-email
```
# Clone a test repository

#if private
```bash
git clone git@github.com:username/test.git
```
#if public
```bash
git clone git://github.com/username/test
```
# Link local and remote repo
```bash
git remote set-url origin git@github.com:username/test.git
```
# Now you can do your stuff...
```bash
touch file
  
git add file
  
# or git add -A 
  
git commit -am "this is a test message"
  
git push
```
