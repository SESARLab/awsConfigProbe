**Moon Cloud Probe for [AWS Config Rule](https://github.com/awslabs/aws-config-rules)**
====================
**Installation**

    # git clone https://github.com/SESARLab/mooncloud_probe_awsconfigrule.git
    # cd mooncloud_probe_awsconfigrule
    # ./install.sh    

**Usage**

Replace XXX in _aws_access_key,aws_secret_access_key,region_ with your AWS credentials
Set which rules you want to check in _rulename_ field (rulename comes for you AWS Config dashboard)

    <collector probe_driver="AWSConfigRuleProbe" id="awstest" cmid="awstest">
        <TestCases>
            <TestCase>
                <ID>1</ID>
                <TestInstance Operation="config">
                    <Input>
                        <Item key="aws_access_key" value="XXX"/>
                        <Item key="aws_secret_access_key" value="XXX"/>
                        <Item key="region" value="XXX"/>
                    </Input>
                </TestInstance>
                <TestInstance Operation="rule">
                    <Input>
                        <Item key="rulename" value="XXX"/>
                    </Input>
                </TestInstance>
            </TestCase>
    
        </TestCases>
    </collector>



Devloped by: filippo.gaudenzi at unimi dot it, github account:[anonymez](https://github.com/anonymez) 