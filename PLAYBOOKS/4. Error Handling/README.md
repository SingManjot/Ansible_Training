# Error Handling in Ansible

## IGNORE_ERRORS
* Lets assume you have 4 tasks defined and have an inventory with 3 VM's. If any task were to fail in any one of the VM's, we stop the playbook all together and don't go forward with the other tasks.

* To solve this, we use the following code in tasks
    ```
    ignore_errors: true
    ```

* Lets say the first task fails on the node 1, If we have the above param set as true, the next set of tasks will be executed on the other nodes and not the node 1.

## FAILED_WHEN
* Usually you can have different errors being printed for the same command.
* This is used to set when you consider the output of a command as failed or no
    ```
    failed_when:
    - '"No such file or directory" not in file_check.stdout'
    ```