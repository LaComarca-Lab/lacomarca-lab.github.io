
# WORK IN PROGRESS


Based on the [Petridish theme](https://github.com/peterdesmet/petridish).

## Quickstart guide

```
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler

git clone https://github.com/LaComarca-Lab/lacomarca-lab.github.io.git

cd lacomarca-lab.github.io

bundle install
```
