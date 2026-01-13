Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"  # Cambia si usas otra distro
  
  # REDIRECCIÓN DE PUERTOS - ESTA ES LA CLAVE
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  # guest: puerto dentro de la VM (donde corre Tomcat)
  # host: puerto en tu máquina (desde donde accederás)
  
  # También añade IP privada para acceso directo
  config.vm.network "private_network", ip: "192.168.56.100"
  
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
  end
  

end