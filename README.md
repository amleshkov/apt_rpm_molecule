### Simple molecule test for custom ansible apt_rpm module
https://github.com/amleshkov/community.general/blob/ADCM-6434_8.6.8/plugins/modules/apt_rpm.py
1. Create venv
2. Install requrements `pip install -r requirements.txt`
3. Clone repository `git clone https://github.com/amleshkov/community.general.git`
4. Checkout branch `cd community.general && git checkout  ADCM-6434_8.6.8`
5. Build collection `ansible-galaxy collection build`
6. Install collection `ansible-galaxy collection install /community.general/community-general-8.6.8.tar.gz`

Build image from `Dockerfile` and fix `test/apt_rpm/roles/main/molecule/default/molecule.yml` and `test/apt_rpm/roles/main/molecule/default/converge.yml` to reduce overhead of `apt-get update` and  installing python3.
