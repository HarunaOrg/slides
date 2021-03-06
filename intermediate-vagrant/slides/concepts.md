# Vagrant Concepts

## *Provider*

- Virtualization software that runs VMs
- *e.g.*
  - **VirtualBox** (default provider)
  - **VMWare Workstation, Fusion**
  - **Hyper-V**
  - **AWS**

!SLIDE

# Vagrant Concepts

## *Host*

- System running virualization software

!SLIDE

# Vagrant Concepts

## *Guest*

- System that is virtualized
- 'VM'

!SLIDE

# Vagrant Concepts

## *Base Box*

- VM configured and packaged for Vagrant
- Intended for sharing w/ others and / or as template from which to create development VMs / boxes
- VM OS is typically Linux

!SLIDE

# Vagrant Concepts

## *Box*

- VM loaded into Vagrant
- initialized, managed, accessed via Vagrant

!SLIDE

# Vagrant Concepts

## *Command-line interface*

- `vagrant`:
  - `$ vagrant init`
  - `$ vagrant up`
  - `$ vagrant ssh`
  - `$ vagrant halt`
  - `$ vagrant destroy`
  - `$ vagrant package`

<!-- vagrant manage boxes, package base boxes, ssh to box -->

!SLIDE

# Vagrant Concepts

## `Vagrantfile`

- Specifies configuration of box instance
- Ruby
- Example:

```ruby
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "sl65-catalog-dev.vb.20140505" # base-box name
  config.vm.hostname = config.vm.box

  config.vm.box_url = "/net/vagrant/ctm/#{config.vm.box}.box" # base-box URL

  config.vm.network "forwarded_port", guest: 3000, host: 3000
end
```

!SLIDE

# Vagrant Concepts

## *Synced Folders*

- Shared filesystem(s) between host system and guest VM
- Coordinates host- and guest-system file-based activities
  - Host filesystem activities
    - editing code
    - version control
  - Guest filesystem activities
    - code is executed by VM
  - *e.g.*
    - edit and `git` code on **OSX** host
    - code is executed on **Linux** guest

!NOTE
This is a key ingredient of Vagrant's 'secret sauce'
