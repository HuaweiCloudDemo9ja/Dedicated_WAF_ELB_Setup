# Dedicated_WAF_ELB_Setup
# Pointing Traffic to an ECS Hosting Your Website

If your origin servers are deployed on **Huawei Cloud ECSs** (NOT BEHIND AN ELB), perform the following steps to configure a security group rule to allow only the back-to-source IP address of the dedicated WAF instance to access the origin servers.

---

## Step 1: Obtain the subnet IP addresses of all dedicated WAF instances

1. Click **☰** in the upper left corner of the page and choose  
   **Web Application Firewall** under **Security & Compliance**.
2. In the navigation pane on the left, choose  
   **Instance Management > Dedicated Engine**.
3. On the **Dedicated Engine** page, click the **IP address** in the **IP Address** column of the dedicated engine and copy the address.

> **Figure 7**: Obtaining the subnet IP address of a dedicated engine  
>

## Step 2: Add the subnet IP address to the ECS security group

1. In the upper left corner of the page, click **☰** and choose  
   **Compute > Elastic Cloud Server**.
2. On the **Elastic Cloud Server** page, click the **target ECS instance name**.
3. On the **ECS details** page, click the **Security Groups** tab and then click **Change Security Group**.
4. On the **Change Security Group** panel displayed, select a security group or create a new one, then click **OK**.
5. Click the **security group ID** and view the details.
6. Click the **Inbound Rules** tab and then click **Add Rule**.
7. In the **Add Inbound Rule** dialog box, configure the parameters as shown in **Table 3**, then click **OK**.

> **Figure 8**: Add Inbound Rule
8. Click OK.
Now, the security group allows all inbound traffic from the back-to-source IP addresses of all your dedicated WAF instances.
