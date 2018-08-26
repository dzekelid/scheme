---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Create workflow scheme
  description: |-
    Create a new workflow scheme.

    The body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/issuesecurityschemes/{id}:
    get:
      summary: Get issue security scheme
      description: Returns the issue security scheme along with that are defined.
      operationId: com.atlassian.jira.rest.v2.issue.IssueSecuritySchemeResource.getIssueSecurityScheme_get
      x-api-path-slug: api2issuesecurityschemesid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Security
      - Scheme
  /api/2/notificationscheme/{id}:
    get:
      summary: Get notification scheme
      description: |-
        Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2notificationschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the notification scheme
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Scheme
  /api/2/permissionscheme:
    post:
      summary: Create permission scheme
      description: Creates a new permission scheme. You can create a permission scheme
        with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionScheme_po
      x-api-path-slug: api2permissionscheme-post
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}:
    get:
      summary: Get permission scheme
      description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionScheme_get
      x-api-path-slug: api2permissionschemeschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to return (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    put:
      summary: Update permission scheme
      description: |-
        Updates a permission scheme. Below are some important things to note when using this resource:

        *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
        *   If you want to update only the name and description, then do not send a permissions list in the request.
        *   Sending an empty list will remove all permission grants from the permission scheme.

        If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.updatePermissionScheme_pu
      x-api-path-slug: api2permissionschemeschemeid-put
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to update (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    delete:
      summary: Delete permission scheme
      description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionScheme_de
      x-api-path-slug: api2permissionschemeschemeid-delete
      parameters:
      - in: path
        name: schemeId
        description: The ID of the permission scheme being deleted (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}/permission:
    get:
      summary: Get permission scheme grants
      description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrants
      x-api-path-slug: api2permissionschemeschemeidpermission-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grants
  /api/2/permissionscheme/{schemeId}/permission/{permissionId}:
    get:
      summary: Get permission scheme grant
      description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrant_
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: permissionId
        description: The ID of the permission grant (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grant
    delete:
      summary: Delete permission scheme entity
      description: Deletes a permission grant from a permission scheme. See [About
        permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
        for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionSchemeEnt
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-delete
      parameters:
      - in: path
        name: permissionId
        description: The ID of the permission grant to delete (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme to delete the permission grant
          from (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Entity
  /api/2/project/{projectKeyOrId}/issuesecuritylevelscheme:
    get:
      summary: Get project issue security scheme
      description: |-
        Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectIssueSecurityLevelSchemeResource.getIssueSecurityScheme_get
      x-api-path-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
      parameters:
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Issue
      - Security
      - Scheme
  /api/2/project/{projectKeyOrId}/notificationscheme:
    get:
      summary: Get project notification scheme
      description: |-
        Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.notification.ProjectNotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2projectprojectkeyoridnotificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Notification
      - Scheme
  /api/2/project/{projectKeyOrId}/permissionscheme:
    get:
      summary: Get assigned permission scheme
      description: |-
        Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.getAssignedPermissionScheme_ge
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Permission
      - Scheme
    put:
      summary: Assign permission scheme
      description: |-
        Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.assignPermissionScheme_put
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Permission
      - Scheme
  /api/2/workflowscheme:
    post:
      summary: Create workflow scheme
      description: |-
        Create a new workflow scheme.

        The body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults.
      operationId: com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.createWorkflowScheme_post
      x-api-path-slug: api2workflowscheme-post
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Scheme
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---