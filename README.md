# Sample repo with example for Extensive Kitchen-Terraform test

## Requirments

Make sure you have the following prerequisites for this tutorial  
  
An AWS Account  
An AWS Access Key ID  
An AWS Secret Key  
An AWS Keypair  
Terraform installed  
Bundler installed  
Ruby 2.3.1  
The default security group on your account must allow SSH access from your IP address

### How to use it:
-   clone the repo
```
git clone https://github.com/chavo1/extensive-kitchen-terraform.git
```
-   download needed gems  
```
$ bundle install
```
-   execute the key.sh script to create needed keys
```
$ ./key.sh
```
-   excute the test.sh script to start test process 
```
$ ./test.sh
```

-   the result from the test should be as follow:
```
Verifying local

Profile: Extensive Kitchen-Terraform (extensive_suite)
Version: 0.1.0
Target:  local://

  ✔  state_file: 0.11.8
     ✔  0.11.8 should match /\d+\.\d+\.\d+/
  ✔  inspec_attributes: static terraform output
     ✔  static terraform output should eq "static terraform output"
     ✔  static terraform output should eq "static terraform output"


Profile Summary: 2 successful controls, 0 control failures, 0 controls skipped
Test Summary: 3 successful, 0 failures, 0 skipped
Verifying host ec2-34-201-134-221.compute-1.amazonaws.com of remote

Profile: Extensive Kitchen-Terraform (extensive_suite)
Version: 0.1.0
Target:  ssh://centos@ec2-X-X-X-X.compute-1.amazonaws.com:22

  ✔  operating_system: centos
     ✔  centos should eq "centos"
  ✔  reachable_other_host: Host X.X.X.X

     ✔  Host X.X.X.X
      should be reachable


Profile Summary: 2 successful controls, 0 control failures, 0 controls skipped
Test Summary: 2 successful, 0 failures, 0 skipped
Verifying host ec2-X-X-X-X.compute-1.amazonaws.com of remote

Profile: Extensive Kitchen-Terraform (extensive_suite)
Version: 0.1.0
Target:  ssh://centos@ec2-X-X-X-X.compute-1.amazonaws.com:22

  ✔  operating_system: centos
     ✔  centos should eq "centos"
  ✔  reachable_other_host: Host X.X.X.X

     ✔  Host X.X.X.X
      should be reachable


Profile Summary: 2 successful controls, 0 control failures, 0 controls skipped
Test Summary: 2 successful, 0 failures, 0 skipped
       Finished verifying <extensive-suite-centos> (0m42.05s).
```
