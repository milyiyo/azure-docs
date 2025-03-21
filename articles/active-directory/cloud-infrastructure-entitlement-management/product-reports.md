---
title: View system reports in the Reports dashboard in CloudKnox Permissions Management
description: How to view system reports in the Reports dashboard in CloudKnox Permissions Management.
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

# View system reports in the Reports dashboard

> [!IMPORTANT]
> CloudKnox Permissions Management (CloudKnox) is currently in PREVIEW.
> Some information relates to a prerelease product that may be substantially modified before it's released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

CloudKnox Permissions Management (CloudKnox) has various types of system report types available that capture specific sets of data. These reports allow management to:

- Make timely decisions.
- Analyze trends and system/user performance.
- Identify trends in data and high risk areas so that management can address issues more quickly and improve their efficiency.

## Explore the Reports dashboard

The **Reports** dashboard provides a table of information with both system reports and custom reports. The **Reports** dashboard defaults to the **System Reports** tab, which has the following details:

- **Report Name**: The name of the report.
- **Category**: The type of report. For example, **Permission**.
- **Authorization Systems**: Displays which authorizations the custom report applies to.
- **Format**: Displays the output format the report can be generated in. For example, comma-separated values (CSV) format, portable document format (PDF), or Microsoft Excel Open XML Spreadsheet (XLSX) format.

    - To download a report, select the down arrow to the right of the report name, or from the ellipses **(...)** menu, select **Download**.

      The following message displays across the top of the screen in green if the download is successful: **Successfully Started To Generate On Demand Report**.

## Available system reports

CloudKnox offers the following reports for management associated with the authorization systems noted in parenthesis:

- **Access Key Entitlements And Usage**:
    - **Summary of report**: Provides information about access key, for example, permissions, usage, and rotation date.
    - **Applies to**: Amazon Web Services (AWS) and Microsoft Azure
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Summary** or **Detailed**
    - **Use cases**:
        - The access key age, last rotation date, and last usage date is available in the summary report to help with key rotation.
        - The granted task and Permissions creep index (PCI) score to take action on the keys.

- **User Entitlements And Usage**:
    - **Summary of report**: Provides information about the identities' permissions, for example, entitlement, usage, and PCI.
    - **Applies to**: AWS, Azure, and Google Cloud Platform (GCP)
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Summary** or **Detailed**
    - **Use cases**:
         - The data displayed on the **Usage Analytics** screen is downloaded as part of the **Summary** report. The user's detailed permissions usage is listed in the **Detailed** report.

- **Group Entitlements And Usage**:
    - **Summary of report**: Provides information about the group's permissions, for example, entitlement, usage, and PCI.
    - **Applies to**: AWS, Azure, and GCP
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Summary**
    - **Use cases**:
         - All group level entitlements and permission assignments, PCIs, and the number of members are listed as part of this report.

- **Identity Permissions**:
    - **Summary of report**: Report on identities that have specific permissions, for example, identities that have permission to delete any S3 buckets.
    - **Applies to**: AWS, Azure, and GCP
    - **Report output type**: CSV
    - **Ability to collate report**: No
    - **Type of report**: **Summary**
    - **Use cases**:
         - Any task usage or specific task usage via User/Group/Role/App can be tracked with this report.

- **Identity privilege activity report**
    - **Summary of report**: Provides information about permission changes that have occurred in the selected duration.
    - **Applies to**: AWS, Azure, and GCP
    - **Report output type**: PDF
    - **Ability to collate report**: No
    - **Type of report**: **Summary**
    - **Use cases**:
        - Any identity permission change can be captured using this report.
        - The **Identity Privilege Activity** report has the following main sections: **User Summary**, **Group Summary**, **Role Summary**, and **Delete Task Summary**.
        - The **User** summary lists the current granted permissions and high-risk permissions and resources accessed in 1 day, 7 days, or 30 days. There are subsections for newly added or deleted users, users with PCI change, and High-risk active/inactive users.
        - The **Group** summary lists the administrator level groups with the current granted permissions and high-risk permissions and resources accessed in 1 day, 7 days, or 30 days. There are subsections for newly added or deleted groups, groups with PCI change, and High-risk active/inactive groups.
        - The **Role summary** lists similar details as **Group Summary**.
        - The **Delete Task summary** section lists the number of times the **Delete task** has been executed in the given time period.

- **Permissions Analytics Report**
    - **Summary of report**: Provides information about the violation of key security best practices.
    - **Applies to**: AWS, Azure, and GCP
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Detailed**
    - **Use cases**:
         - This report lists the different key findings in the selected auth systems. The key findings include super identities, inactive identities, over provisioned active identities, storage bucket hygiene, and access key age (for AWS only). The report helps administrators to visualize the findings across the organization.

    For more information about this report, see [Permissions analytics report](product-permissions-analytics-reports.md).

- **Role/Policy Details**
    - **Summary of report**: Provides information about roles and policies.
    - **Applies to**: AWS, Azure, GCP
    - **Report output type**: CSV
    - **Ability to collate report**: No
    - **Type of report**: **Summary**
    - **Use cases**:
         - Assigned/Unassigned, custom/system policy, and the used/unused condition is captured in this report for any specific, or all, AWS accounts. Similar data can be captured for Azure/GCP for the assigned/unassigned roles.

- **PCI History**
    - **Summary of report**: Provides a report of privilege creep index (PCI) history.
    - **Applies to**: AWS, Azure, GCP
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Summary**
    - **Use cases**:
         - This report plots the trend of the PCI by displaying the monthly PCI history for each authorization system.

- **All Permissions for Identity**
    - **Summary of report**: Provides results of all permissions for identities.
    - **Applies to**: AWS, Azure, GCP
    - **Report output type**: CSV
    - **Ability to collate report**: Yes
    - **Type of report**: **Detailed**
    - **Use cases**:
         - This report lists all the assigned permissions for the selected identities.




## Next steps

- For a detailed overview of available system reports, see [View a list and description of system reports](all-reports.md).
- For information about how to create, view, and share a system report, see [Create, view, and share a custom report](report-view-system-report.md).
- For information about how to create and view a custom report, see [Generate and view a custom report](report-create-custom-report.md).
- For information about how to create and view the Permissions analytics report, see [Generate and download the Permissions analytics report](product-permissions-analytics-reports.md).
