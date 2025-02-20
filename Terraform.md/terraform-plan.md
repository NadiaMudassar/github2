# Terrafrom Plan

The `terraform plan` command is a fundamental tool in Terraform's workflow, allowing you to preview the changes that Terraform will make to your infrastructure based on the current configuration files. This step is crucial for understanding the impact of your changes before applying them.

**Understanding `terraform plan`:**

- **Purpose:** Generates an execution plan, detailing the actions Terraform will take to align your infrastructure with the desired state defined in your configuration files. citeturn0search1

- **Output:** Displays a summary of actions, including resources to be created, modified, or destroyed, along with their attributes.

**Example Workflow:**

1. **Initialize Terraform:** Ensure your working directory is initialized with the necessary provider plugins.

   ```bash
   terraform init
   ```

2. **Validate Configuration:** Check the syntax and internal consistency of your configuration files.

   ```bash
   terraform validate
   ```

3. **Generate Execution Plan:** Preview the changes Terraform will make.

   ```bash
   terraform plan
   ```

   This command will output a detailed plan, indicating the actions Terraform will perform, such as creating a resource group named `my_demo_RG_one` in the `East US` region.

4. **Apply Changes:** Execute the planned actions to modify your infrastructure.

   ```bash
   terraform apply
   ```

   Terraform will prompt for confirmation before proceeding.

![Terraform plan ](<Images/Screenshot 2025-02-18 195051.png>)

**Best Practices:**

- **Review Plans Carefully:** Always examine the output of `terraform plan` to ensure the proposed changes align with your intentions.

- **Use Plan Files:** For automation or team environments, save the plan to a file and apply it later to ensure consistency.

  ```bash
  terraform plan -out=tfplan
  terraform apply tfplan
  ```

- **Automate with Caution:** While automating with flags like `-auto-approve` can be convenient, it bypasses manual confirmation and should be used judiciously.

By incorporating `terraform plan` into your workflow, you can confidently manage infrastructure changes, ensuring they are intentional and aligned with your desired state.

For a more in-depth understanding, you might find the following video helpful:

[Using the terraform plan Command (Lightboard)](https://www.youtube.com/watch?v=Ib9p6pYgfc4)
