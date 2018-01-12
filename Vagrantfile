# -*- mode: ruby -*-
# vi: set ft=ruby :
 
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define "win1" do |win1|
    win1.vm.guest = :windows
    win1.vm.box = "win10_1709"
    win1.vm.communicator = "winrm"
    win1.vm.boot_timeout = 600
    win1.vm.graceful_halt_timeout = 600
 
    # Create a forwarded port mapping which allows access to a specific port
    # within the machine from a port on the host machine. In the example below,
    # accessing "localhost:8080" will access port 80 on the guest machine.
    # config.vm.network "forwarded_port", guest: 80, host: 8080
    win1.vm.network :forwarded_port, guest: 3389, host: 3391
    win1.vm.network :forwarded_port, guest: 5985, host: 5985, id: "winrm", auto_correct: true
  end
end

