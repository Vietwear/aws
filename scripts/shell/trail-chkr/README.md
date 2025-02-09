### Check CloudTrail Status

<p>
This BASH script checks the name and status of CloudTrail in all regions of your AWS account.

<b>Requirements:</b>
<ul>
 <li> The awscli  (`sudo pip install awscli`)
 <li> A valid profile in ~/.aws/config or ${AWS_CONFIG_FILE} with the appropriate API keys
</ul>

<b>Usage:</b>
<p>
<pre>
Usage: trail-chkr.sh -p &lt;profile_name&gt; [ -d ]

  -p  : profile name (in ~/.aws/config)
  -d  : (optional) delete trails
  
</pre>

<b>Output:</b>
<p>
<pre>
./trail-chkr.sh -p eng

Checking us-east-1...
CloudTrail Name: eng-cloudtrail-logs-ue1
Enabled: True

Checking eu-west-1...
CloudTrail Name: eng-cloudtrail-logs-ew1
Enabled: True

Checking ap-northeast-1...
CloudTrail Name: eng-cloudtrail-logs-an1
Enabled: True

Checking us-west-1...
CloudTrail Name: eng-cloudtrail-logs-uw1
Enabled: True

Checking us-west-2...
CloudTrail Name: eng-cloudtrail-logs-uw2
Enabled: True

Checking ap-southeast-1...
CloudTrail Name: eng-cloudtrail-logs-as1
Enabled: True

Checking ap-southeast-2...
CloudTrail Name: eng-cloudtrail-logs-as2
Enabled: True

Checking sa-east-1...
Enabled: False

Happy trails!
</pre>

<b>To Do:</b>
<ul>
 <li> Replace the REGIONS variable with a dynamic array. Build with the `aws ec2 describe-regions` command
</ul>
