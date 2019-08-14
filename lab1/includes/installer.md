<section id="requirements" class="section"> 

**NOTE**: You must have [chocolatey](https://chocolatey.org/docs/installation#installing-chocolatey) installed before proceeding!

<form class="docforms" action>

<ul>

<li><input id="all" type="checkbox" data-wait="1" class="selectall" data-group="tools" /><label class="selectall" for="all">Mark All For Installation</label></li>

<ul>
<li><input id="cmder" type="checkbox" data-wait="1" class="child" data-cmd-command="C:\\ProgramData\\chocolatey\\bin\\choco.exe install -y cmder" data-group="tools" /><label for="cmder">Install cmder</label></li>
<li><input id="sublime" type="checkbox" data-wait="1" class="child" data-cmd-command="C:\\ProgramData\\chocolatey\\bin\\choco.exe install -y sublimetext3.app" data-group="tools" /><label for="sublime">Install Sublime Text 3</label></li>
<li><input id="virtualbox" type="checkbox" data-wait="1" data-cmd-command="C:\\ProgramData\\chocolatey\\bin\\choco.exe install -y virtualbox" class="child" data-group="tools" /><label for="virtualbox">Install Virtualbox</label></li>
<li><input id="vagrant" type="checkbox" data-wait="1" data-cmd-command="C:\\ProgramData\\chocolatey\\bin\\choco.exe install -y vagrant" class="child" data-group="tools" /><label for="vagrant">Install Vagrant</label></li>
</ul>

<input type="hidden" name="form_id" value="170039" /> <input id="saveForm" class="button_text" type="button" name="submit" value="Submit" onClick="javascript:install();" /></li>

</ul>

</form>

</section>