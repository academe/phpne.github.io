Vagrant.configure("2") do |config|
    config.vm.box = "trusty64"
    config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    config.vm.hostname = "phpne-org-uk"
    config.vm.network :forwarded_port, guest: 4000, host: 4000
    config.vm.provider :virtualbox do |virtualbox|
        virtualbox.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]
    end
    config.vm.provision :shell, :path => "_env/provision.sh"
end
