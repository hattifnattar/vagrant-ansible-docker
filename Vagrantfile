Vagrant.configure("2") do |config|
  config.vm.define "ansible" do |web|
    web.vm.box = "centos/7"
    web.vm.hostname = 'ansible'
    web.vm.box_url = "centos/7"

    web.vm.network :private_network, ip: "192.168.7.100"

    web.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "ansible"]
    end
  end

  config.vm.define "test" do |db|
    db.vm.box = "centos/7"
    db.vm.hostname = 'test'
    db.vm.box_url = "centos/7"

    db.vm.network :private_network, ip: "192.168.7.101"

    db.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "test"]
    end
  end
end
