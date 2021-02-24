<h1> Playing with Git</h1>

<h2> Purpose</h2>

<p> To get used to the main git commands in conjunction with GitHub, and pushing/pulling content between GitHub and my local repos. There's really not much to see in terms of other file content. The main thing here is the explanation in this ReadMe of how I produced the simple text manipulation.

<h2> Getting set up locally</h2>

<p><i>Note: I use Linux (Ubuntu). Where " is used, this means you need to supply specific information only you know e.g. email addresses, file names</i></p>

<ul>
    <li><i>Make sure git is installed on system.</i> This can be checked with <code>$ git --version</code> </li>
    <li><i>Configure git with your personal info</i> <code>$ git config --global user.name "your name"</code> then <code>$ git config --global user.email "your email"</code></li>
    <li><i>Formal settings.</i> <code>$ git config --global core.autocrlf input</code> <code>git config --global core.safecrlf true</code> </li>
    <li><i>Set up a local folder which will become a git repository (repo)</i> You can do this where you want, but you will be using <code>cd</code> to navigate <code>mkdir</code> to make your folder and either <code>echo</code> or <code>touch</code> when making a simple text file </li>
    <li><i>Make your folder a git repository by initialising git.</i> This will add some files, in a folder called .git <code>$ git init</code> </li>
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
    <li><code>git status</code> which gives an overview of what has changed (if anything) since the last commit</li>
    <li><code>git log</code> which shows information about previous commits, including giving them a specific, unique identifier</li>
    <li><code>git checkout "CommitHash"</code> which returns the directory to the state at the time of the commit being referenced</li>
    <ul>
            <li>
                Note: You don't actually have to use the full hash, just 4+ characters, as long as they give an unambniguous reference, so one that isn't shared with other commits.
            </li>
        </ul>
</ul>
    
<h2> Integrating with GitHub</h2>

<p> Here are the main commands that I used once set up.:

<ul>
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
</ul>
