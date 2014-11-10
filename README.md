## VagrantとAnsibleを使用して開発用サーバを構築する

### 仮想マシンの準備
#### 1.virtual boxをインストール
	
	下記のURLから適切なvirtual boxをダウンロードし、インストールする
	URL: https://www.virtualbox.org/wiki/Downloads

#### 2.vagrantをインストール
	
	下記のURLからvagrantをダウンロードし、インストールする
	URL: https://www.vagrantup.com/downloads.html

#### 3.ローカルで作業用ディレクトリを作成（任意）
	
	mkdir ~/Vagrant
	cd ~/Vagrant

#### 4.boxの追加

	vagrant box add Ubuntu1404 https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box

	追加するBOXのURLは下記を参照
	URL: http://www.vagrantbox.es/

#### 5.仮想マシンを作成

	vagrant init Ubuntu1404

#### 6.仮想マシンを起動

	vagrant up

#### 7.仮想マシンに接続

	vagrant ssh

### Ansibleの設定
#### 1.Ansibleのパッケージを検索

	apt-cache serch ansible

	ansible - Configuration management, deployment, and task execution system
	ansible-doc - Ansible documentation and examples
	ansible-fireball - Ansible fireball transport support
	ansible-node-fireball - Ansible fireball transport support for nodes
	python-reclass - hierarchical inventory backend for configuration management systems
	reclass - hierarchical inventory backend for configuration management systems

#### 2.Ansibleをインストール
検索して１番上に出てきたパッケージをインストールします。

	sudo apt-get install ansible

#### 3.インストールできたか確認

	which ansible

	/usr/bin/ansible

