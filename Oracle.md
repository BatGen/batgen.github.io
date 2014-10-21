---
layout: page
title: Oracle XE Database
header: Oracle XE Database
--- 
<div class="col-md-3"
    style="text-align: center; list-style-type: square;">
    <h1>Oracle XE Database</h1>
    <br>
    <h3>Other Databases</h3>
    <ul style="text-align: left">
        <li><a href="../H2.html" >H2</a></li>
    </ul>
</div>

<div class="col-md-9">
    <div>
        <h3>How do I set up Oracle XE Database?</h3>
		
		<ol>
			<li><a http://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html" target="_blank">
			Download</a> the correct release for your machine.</li>
			
			<li>Unzip the folder and run setup.exe to install Oracle XE.</li>
			
			<li>When asked where to install, chose a location for the folder.</li>
			
			<li>When asked to create a password, use '123'. So it would be same as all others.</li>
			
			<li>When finished installing, start the 'Get Started with Oracle ..." that appeared on the Desktop.</li>
			
			<li>Within the browser, click on 'Application Express' and login as System with password 123.</li>
			
			<li>Fill in the following information:
				<ul>
					<li>Database User: Create New</li>
					<li>Database Username: sa</li>
					<li>Application Express Username: batgen</li>
					<li>Password: 123</li>
					<li>Confirm Password: 123</li>
				</ul>
				Click on create Workspace.
			</li>
			
			<li>You will get a message telling you that a workspace is successfully created, and click there to login.
			You can also click on 'Application Express', and then click on 'Already have an account? Login here'.</li>
			
			<li>Login with the information that was used to create the workspace.</li>
			
			<li>Click on the 'SQL Workshop'.</li>
			<li>OPTIONAL but recommended: click on 'Object Browser', select one of the 
			tables on the left, and the click on Drop on the right. Select 
			'Cascade Constraints' and click 'Finish'. Repeat this for all the tables 
			until the list is empty. Now do this for 'Sequences' and 'Functions' on the drop-down list.</li>
			
			<li>Under 'SQL Workshop', click on 'SQL Commands'. </li>
			
			<li>Oracle XE does not take multiple commands at once, so commands have to be
			entered one at a time. Get the commands from Eclipse, under the sql folder, 
			the CreateTables.sql file.
			
				<ul>Example:
				<li>1st command: 
{% highlight ruby %}
create table EMPLOYEE (
    EMPLOYEE_KEY       NUMBER(10) not null,
    SALARY             NUMBER(10,2),
    LAST_NAME          VARCHAR2(132),
    FIRST_NAME         VARCHAR2(132),
    SUPERVISOR_KEY     NUMBER(10),
    constraint EMPLOYEE_PK primary key (EMPLOYEE_KEY)
);
{% endhighlight %}
				</li>
				<li>2nd command:
{% highlight ruby %}
create sequence EMPLOYEE_SEQ;
{% endhighlight %}
				</li>
				And so on, till all of the commands on CreateTables.sql had ran.
				</ul>
				
			</li>
			
			<li>Now the database is ready for use. On Eclipse, add the OracleDriver to 
			the build path. Right click on project, click 'Properties' and select 
			'Java Build Path'. Click on 'Libraries' and then click on 'Add External JARs..'.
			The OracleDriver is located in the installed folder, app/oracle/product/11.2.0/server/jdbc/lib.
			Select the ojdbc6 jar and click done.</li>
			
			<li>To turn database on or off, click on the window start menu -> 
			All Programs -> Oracele Database xxg Express Edition -> Get Started.</li>
		</ol>
		
		
    </div>
</div>