<h1>Getting Started with AWS CodePipeline and CrossBrowserTesting</h1>
<p><em>For this document, we provide an example Lambda Function located in our <a href="https://github.com/crossbrowsertesting/selenium-aws_codepipeline">AWS CodePipline Github Repository</a>.</em></p>
<p><a href="https://aws.amazon.com/codepipeline/">AWS CodePipeline</a> is a continuous delivery  tool that lets you automate your development process quickly, safely, and at scale. Through AWS CodePipeline’s integration with many other AWS and third party services such as ECS, S3, Elastic Beanstalk, CloudFormation GitHub, and Jenkins, every time you commit code, a build is created and automatically run, allowing you to test every commit.</p>
<p>In this guide we will use AWS CodePipeline with Github and an AWS Lambda Function for testing using the <a href="https://www.seleniumhq.org/">Selenium Webdriver</a> and the <a href="https://www.javascript.com/">Javascript</a> programming language.</p>
<h3>Creating an AWS Lambda Function</h3>
<p>1. Navigate to https://console.aws.amazon.com/lambda/</p>
<p>2. Click the Create Function button</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/aws_create_function.png" /></p>
<p>3. Name your function and click the Create Function button</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/aws_name_function.png" /></p>
<p>4. Download the example <a href="https://github.com/crossbrowsertesting/selenium-aws_codepipeline/blob/master/lambda_function.zip">Lambda Function</a>, and choose 'Upload a .zip file' from the 'Code entry type' dropdown in the Function Code section</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/aws_zipfile.png" /></p>
<p>5. Set your username and authkey as environment variables</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/aws_upload_zipfile_and_env_vars.png" /></p>
<p>6. Set your execution role and basic settings then click 'Save'</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/aws_execution_role_and_settings.png" /></p>
<h3>Setting Up AWS CodePipeline</h3>
<p>1. Navigate to the <a href="https://console.aws.amazon.com/codesuite/codepipeline/home?p=cpl&amp;cp=bn&amp;ad=c">AWS CodePipeline homepage</a></p>
<p>2. Click the 'Create pipeline' button</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/AWS_create_pipeline.png" /></p>
<p>3. Name your Pipeline and click 'Next'</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/AWS_pipeline_name.png" /></p>
<p>4. Select Github from the Source provider dropdown, click the 'Connect to GitHub' button, chose your repository and branch, then click Next</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/AWS_add_source2.png" /></p>
<p>5. Add any additional desired steps, click 'Next', and then 'Create Pipeline' </p>
<p>6.  Edit you pipeline to add a Lambda stage by clicking the 'Edit'-&gt; 'Add Stage-&gt;Add action group'</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/AWS_add_stage.png" /></p>
<p>7. Name your Action, Choose AWS Lambda as the 'Action Provider', set your Function name and User parameters, and click 'Done'</p>
<p><img src="http://help.crossbrowsertesting.com/wp-content/uploads/2019/11/AWS_action_provider2.png" /></p>
<p>8. Save your pipeline and commit to your repository.</p>
<p>Congratulations! You have successfully integrated CBT and AWS CodePipeline. Now you are ready to see your test run in our <a href="https://app.crossbrowsertesting.com/selenium/results">app.</a></p>
<h3>Conclusion</h3>
<p>By following the steps outlined in this guide, you are now able to seamlessly integrate AWS CodePipeline and CrossBrowserTesting. If you have any questions or concerns, please feel free to reach out to our <a href="mailto:support@crossbrowsertesting.com">support team</a>.</p>
