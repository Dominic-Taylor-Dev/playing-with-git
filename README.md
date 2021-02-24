<h1> Playing with Git</h1>

<h2> Purpose</h2>

<p> To get used to the main git commands in conjunction with GitHub, and pushing/pulling content between GitHub and my local repos. There's really not much to see in terms of other file content. The main thing here is the explanation in this ReadMe of how I produced the simple text manipulation, although you will see from commit history a bit of what I'm talking about.

<h2> Getting set up locally</h2>

<p><i>Note: I use Linux (Ubuntu). Where " is used, this means you need to supply specific information only you know e.g. email addresses, file names</i></p>

<ul>
    <li><i>Make sure git is installed on system.</i> This can be checked with <code>$ git --version</code> </li>
    <li><i>Configure git with your personal info</i> <code>$ git config --global user.name "your name"</code> then <code>$ git config --global user.email "your email"</code></li>
    <li><i>Format settings.</i> <code>$ git config --global core.autocrlf input</code> <code>git config --global core.safecrlf true</code> </li>
    <li><i>Set up a local folder which will become a git repository (repo)</i> You can do this where you want, but you will be using <code>cd</code> to navigate <code>mkdir</code> to make your folder and either <code>echo</code> or <code>touch</code> when making a simple text file </li>
    <li><i>Make your folder a git repository by initialising git within in.</i> This will add some files, in a folder called .git <code>$ git init</code> </li>
    <li><i>Commit locally.</i> Add your file to the 'staging area' <code>$ git add "FileName"</code> and then commit it to the master branch<code>git commit -m "First commit"</code> 
        <ul>
            <li>
                Note: If you remove files, (e.g. <code>rm "FileName"</code>) this also needs to be staged and committed, just like an addition.
            </li>
        </ul>
    </li>
</ul>

<p> Once you've got this far, you're basically set up. There are a few other commands you'll want to know, though:</p>

<ul>
    <li><code>git add "FileName"</code> which adds files to the staging area (meaning they're being tracked but not yet committed)</li>
    <li><code>git rm "FileName"</code> which is the same thing but for when you're removing files</li>
 <li><code>git commit -m "MessageContent"</code> which commits everything in the staging area, along with a message where you can explain what has changed since the last commit</li>
    <li><code>$ git status</code> which gives an overview of what has changed (if anything) since the last commit</li>
    <li><code>$ git log</code> which shows information about previous commits, including giving them a specific, unique identifier</li>
    <li><code>git checkout "CommitHash"</code> which returns the directory to the state at the time of the commit being referenced</li>
    <ul>
            <li>
                Note: You don't actually have to use the full hash, just 4+ characters, as long as they give an unambniguous reference, so one that isn't shared with other commits.
            </li>
        </ul>
</ul>
    
<h2> Pushing your local git to GitHub</h2>

<h3>Connecting to GitHub with SSH</h3>
<p>This is already well explained <a href = "https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh">here<a></p>
    
<h3> Interacting with GitHub</h3>
<p><ul>
    
<li>Firstly, you'll want to set up a new repo in GitHub (manually, by logging in and clicking on "New Repository". I called it "playing-with-git" (this repo!).</li>
 
<li>You're then ready to connect to the remote repo on your local computer. Do that with <code>$ git remote add origin "YourRepoSSHAddress"</code> (the word 'origin' is setting the name of the remote repo in your local repo - you could use something different and it would still work). The repo address should be the same as your SSH clone address. At the moment that's under a dropdown for me called 'Code' on the main page of the repo in GitHub.</li>

<li>Once conntected, you can push (transfer) your local repo to Github (it'll go to the address you set in the last step) using <code>$ git push -u origin master</code></li>

</ul></p>

<h2> Pulling code from GitHub</h2>

If there's anyone else working on your repo, or there are pushes to GitHub that do not come from your local computer - maybe you are working on a different computer yourself - you'll get your files out of sync. For this reason, you'll want to be able to fetch data from GitHub as well as push to it. This is called 'pull' and can be done (within the local repo on the terminal) with <code>$ git pull origin master</code> (assuming you called the remote repo 'origin').
