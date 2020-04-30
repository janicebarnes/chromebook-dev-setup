# Setting up a Chromebook for Linux Web Development

Let’s just say you are “between” computers - your current desktop/laptop is too outdated to become your day to day Linux web development machine. You’re waiting for a price drop, a new processor chip or a new model to be released. Whatever the reason, you are not purchasing your dream web development machine at this time.

So what do you do in the meantime to start coding? You use your Chromebook!

You found this github page because you decided to enable the Linux shell on your Chromebook and set up a Linux web development environment. 

My Lenovo C330 has an aarch64 (ARM64) processor which made it a little tricky to get some packages installed as most packages are made for the x86_64 (AMD64) processor. You can browse to chrome://system or visit https://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices to determine which processor your chromebook has.

This readme is intended as a quick reference of what I did to configure the Linux environment for web development on my Chromebook.

# Steps

1. Enable the Linux shell as per https://support.google.com/chromebook/answer/9145439

2. Make sure your have the correct permissions in the Linux shell with your Chromebook account
<pre><code>sudo usermod -aG sudo yourchromebookaccountname</code></pre>

3. Install Node and NPM (https://support.google.com/chromebook/thread/26505720)
<pre><code>
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt install nodejs
sudo apt-get upgrade && sudo apt-get update
</code></pre>

4. I chose to install Typescript and VueJS. You are free to install the language and framework of your choice, i.e. react, angular, etc.
<pre><code>sudo npm install -g typescript
sudo npm install -g @vue/cli</code></pre>

5. Install basic Git tools
<pre><code>sudo apt-get update
sudo apt-get install git</code></pre>

5.5 Configure Git
<pre><code>
git config --global user.name "your name"
git config --global user.email "your email"
</code></pre>

6. Install Visual Studio Code editor

If you have AMD64 (https://code.visualstudio.com/download):
<pre><code>
sudo apt install ./fileyoudownloaded.deb
</pre></code>
If you have AARCH64 (http://code.headmelted.com/#linux-install-scripts):
<pre><code>
sudo -s
 . <( wget -O - https://code.headmelted.com/installers/apt.sh )
 </pre></code>

7. Here are some great Visual Studio Code extensions that most developers won't code without:

<ul>
  <li>Babel</li>
<li>ESLint</li>
<li>Prettier Code Formatter</li>
<li>Vetur (for vue)</li>
<li>Vue snippets</li>
<li>GitLens</li>
<li>REST Client</li>
<li>Debugger for Chrome</li>
<li>Live Server</li>
<li>Live SASS compiler</li>
<li>HTML CSS Support</li>
</ul>


Happy coding!
