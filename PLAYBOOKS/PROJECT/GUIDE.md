## Task 1

1. First create IAM user for ansible to access aws. Attach policies for ec2 to allow it to make instances.

2. Then create an access key and secret access key

3. pip install boto3 (pre-req to use aws ansible collection)

4. ansible-galaxy collection install amazon.aws

5. setup ansible vault and store the access key and secret-access-key in the vault
    * To create the first the file that protects the vault: 
        ```
        openssl rand -base64 2048 > vault.paas
        ```
        this will create a base64 encoded password file.
    
    * Now we create a file in the vault, add the secrets in it and lock it with the above created file
        ```
        ansible-vault create gorup_vars/all/paas.yml --vault-password-file vault.pass
        ```
        This vault.pass will be provided as an input to the ansible-playbook command to unlock the vault
    NOTE: PAAS.YAML CREATED JUST FOR DEMONSTRATION IN THIS FOLDER HENCE IT IS EMPTY

6. Run
    ```
    ansible-playbook ansible_ec2_create.yaml --vault-password-file vault.paas
    ```


## Task 2
```
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```

## Task 3
```
ansible-playbook -i inventory.ini ansible_ev2_stop.yaml
```