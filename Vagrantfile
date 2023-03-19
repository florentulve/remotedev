Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/kinetic64"
  config.env.enable
  
  config.vm.provider :virtualbox do |vb|
    vb.name = "devworkspace"
    vb.memory = 4096
    vb.cpus = 16
    vb.gui = false
  end

  # cloud-init script
  config.vm.cloud_init do |cloud_init|
    # With Ubuntu cloud images you have to use cloud_init to get an access
    cloud_init.content_type = "text/cloud-config"
    cloud_init.path = "cloud-init.yml"
  end

end
