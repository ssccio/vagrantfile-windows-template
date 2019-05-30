# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "win" do |win|
    win.vm.box = "sscc/win2016"
    win.vm.guest = :windows
    win.vm.hostname = "win"
    win.vm.communicator = "winrm"
    win.winrm.username = "vagrant"
    win.winrm.password = "vagrant"

    win.vm.network "public_network"

    win.vm.provider "vmware_desktop" do |vm|
      # Display the GUI when booting the machine
      vm.gui = true
      vm.vmx["ethernet0.pcislotnumber"] = "33"

      # Customize the amount of memory on the VM:
      vm.memory = "4096"
    end
  end

end
