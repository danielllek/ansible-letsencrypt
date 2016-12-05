# ansible-letsencrypt
sample role that uses letsencrypt ansible module (2.2 and higher)

Assumptions:
- generate ssl keys/cert on localhost (place where you run ansible)
- upload only key/cert to www host

Important before you start:
- set {{ upload_files_to }} to host you deal with ssl (I use reverse proxy to offload ssl traffic)
- generate your account.key for use with Let's Encrypt
- set variables:
  gen_cert: True

  certaltnames:
    - 'domain.com'
    - 'www.domain.com'
    - 'anotherdomain.com'
    - 'www.anotherdomain.com'

