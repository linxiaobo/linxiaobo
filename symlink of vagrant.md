# Error for Symlink `ln -s` in Vagrant ssh

I have a project that need just add module to a separated repository, so I want to develop in a folder outside the project then symlink to the project to run and test.
I use Vagrant for development, but in Vagrant ssh, I got "Input / Output error" when try to `ln -s development_directory project_directory`, after hours searching in Google and try, got solution below in my case.

## 1. Add symlink access to `Vagrantfile`
```
config.vm.provider "virtualbox" do |v|
    v.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]
end
```
## 2. Set windows to have access to use Symlink

To open Local Security Policy, on the Start screen, type `secpol.msc`, and then press ENTER.
Under Security Settings of the console tree, do one of the following:

Click Local Policies to edit User Rights Assignment, add current user/usergroup to this record.

## 3. Restart the computer

## 4. Now it's ok to run the symlink command "ln -s" in Vagrant ssh.
