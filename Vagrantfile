Vagrant.configure("2") do |config|
  config.vm.communicator = "winrm"
  config.vm.box = "StefanScherer/windows_2019"
  config.vm.box_version = "2020.02.12"

  config.vm.provider "virtualbox" do |v|
    v.gui = true
    v.customize ["modifyvm", :id, "--memory", 2048]
    v.customize ["modifyvm", :id, "--cpus", 2]
    v.customize ["modifyvm", :id, "--vram", 128]
    v.customize ["modifyvm", :id, "--accelerate3d", "on"]
    v.customize ["modifyvm", :id, "--accelerate2dvideo", "on"]
  end

  config.vm.provision "RunCalcExe", type: "shell", path: "run.ps1", privileged: false
end
