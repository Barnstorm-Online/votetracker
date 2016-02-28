# Vote Tracker

## Dependencies

The following will need to be installed on your local development machine before
you can use this workflow. All versions should be the latest available, as some
required features may not be available in older versions.

### Required for Development

* **[node.js 4.3.x](https://nodejs.org/)**
  - [Download](https://nodejs.org/) (All platforms)
  - Install `node` via [homebrew][homebrew]
* **[Ansible](http://docs.ansible.com/) 2.x**
  - Install `ansible` via apt (Ubuntu), yum (Fedora), [homebrew][homebrew] (OS
    X), etc. See the [Ansible installation
    instructions](http://docs.ansible.com/intro_installation.html) for detailed,
    platform-specific information.
* **[VirtualBox](https://www.virtualbox.org/)**
  - [Download](https://www.virtualbox.org/wiki/Downloads) (All platforms)
  - Install `virtualbox` via [homebrew cask][cask] (OS X)
* **[Vagrant](https://www.vagrantup.com/)**
  - [Download](http://docs.vagrantup.com/v2/installation/) (All platforms)
  - Install `vagrant` via [homebrew cask][cask] (OS X)
* **[vagrant-hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater)**
  - Install with `vagrant plugin install vagrant-hostsupdater` (All platforms)

[homebrew]: http://brew.sh/
[cask]: http://caskroom.io/

## Development

1. Run `npm install` to install local dependencies.
2. Run `vagrant up` to set up postgresql database.
3. Run `npm run migrate` to initialize the database model.
3. Run `npm start` to start the file-watcher, api and live-reload process.
4. Browse to <http://localhost:8080/> for the client.
5. Browse to <http://localhost:8000/> for the server.
6. Edit files in `src/client` to see things update automatically.
7. Edit files in `src/server` and the server will automatically restart.

## Production Notes

In production, the server component is mounted at:
http://votetracker.gnarf.net/api
