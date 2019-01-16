# error of Symlink `ln -s` on Vagrant ssh

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
