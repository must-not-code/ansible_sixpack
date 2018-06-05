# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/xenial64'

  config.vm.provider 'virtualbox' do |vm|
    vm.memory = 1024
    vm.cpus   = 1
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'sixpack.yml'
    ansible.extra_vars = {sixpack_password: 'password'}
  end

  config.vm.network 'forwarded_port', guest: 80, host: 8080
  config.vm.network 'forwarded_port', guest: 8080, host: 8081
end
