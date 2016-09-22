Repo Info
=========
Build [Docker] image for [Graphite] provisioned via [Ansible]

Consuming
---------
```
docker run -d -p 2003:2003 -p 2003:2003/udp -p 2004:2004 -p 7002:7002 \
  mrlesmithjr/graphite
```
Spin-up with persistent data for Graphite:
```
docker run -d -p 2003:2003 -p 2003:2003/udp -p 2004:2004 -p 7002:7002 \
  -v $PWD/.data:/var/lib/graphite/whisper mrlesmithjr/graphite
```

Once the container is spun-up and running you can connect
to http://IpOrHostname using your browser. You can now
configure your remote hosts to send Graphite data to tcp/2003
on your container host IpOrHostname.

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- [@mrlesmithjr]
- [everythingshouldbevirtual.com]
- [mrlesmithjr@gmail.com]


[Ansible]: <https://www.ansible.com/>
[Docker]: <https://www.docker.com>
[Graphite]: <https://graphiteapp.org/>
[@mrlesmithjr]: <https://twitter.com/mrlesmithjr>
[everythingshouldbevirtual.com]: <http://everythingshouldbevirtual.com>
[mrlesmithjr@gmail.com]: <mailto:mrlesmithjr@gmail.com>
