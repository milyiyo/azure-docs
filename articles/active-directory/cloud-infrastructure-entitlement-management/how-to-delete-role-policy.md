---
title: Delete a role/policy in the Remediation dashboard in Permissions Management
description: How to delete a role/policy in the Just Enough Permissions (JEP) Controller.
services: active-directory
author: kenwith
manager: rkarlin
ms.service: active-directory
ms.subservice: ciem
ms.workload: identity
ms.topic: how-to
ms.date: 02/23/2022
ms.author: kenwith
---

# Delete a role/policy in the Remediation dashboard

> [!IMPORTANT]
> Microsoft Entra Permissions Management is currently in PREVIEW.
> Some information relates to a prerelease product that may be substantially modified before it's released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

This article describes how you can use the **Remediation** dashboard in Permissions Management to delete roles/policies for the Amazon Web Services (AWS), Microsoft Azure, or Google Cloud Platform (GCP) authorization systems.

> [!NOTE]
> To view the **Remediation** dashboard, you must have **Viewer**, **Controller**, or **Administrator** permissions. To make changes on this tab, you must have **Controller** or **Administrator** permissions. If you don't have these permissions, contact your system administrator.

> [!NOTE]
> Microsoft Azure uses the term *role* for what other Cloud providers call *policy*. Permissions Management automatically makes this terminology change when you select the authorization system type. In the user documentation, we use *role/policy* to refer to both.

## Delete a role/policy

1. On the Permissions Management home page, select the **Remediation** tab, and then select the **Role/Policies** subtab.
1. Select the role/policy you want to delete, and from the **Actions** column, select **Delete**.

    You can only delete a role/policy if it isn't assigned to an identity.

    You can't delete system roles/policies.

1. On the **Preview** page, review the role/policy information to make sure you want to delete it, and then select **Submit**.

## Next steps


- For information on how to view existing roles/policies, requests, and permissions, see [View roles/policies, requests, and permission in the Remediation dashboard](ui-remediation.md).
- For information on how to create a role/policy, see [Create a role/policy](how-to-create-role-policy.md).
- For information on how to clone a role/policy, see [Clone a role/policy](how-to-clone-role-policy.md).
- For information on how to modify a role/policy, see Modify a role/policy](how-to-modify-role-policy.md).
- To view information about roles/policies, see [View information about roles/policies](how-to-view-role-policy.md).
- For information on how to attach and detach permissions for AWS identities, see [Attach and detach policies for AWS identities](how-to-attach-detach-permissions.md).
- For information on how to revoke high-risk and unused tasks or assign read-only status for Azure and GCP identities, see [Revoke high-risk and unused tasks or assign read-only status for Azure and GCP identities](how-to-revoke-task-readonly-status.md)
- For information on how to create or approve a request for permissions, see [Create or approve a request for permissions](how-to-create-approve-privilege-request.md).
- For information on how to view information about roles/policies, see [View information about roles/policies](how-to-view-role-policy.md)
