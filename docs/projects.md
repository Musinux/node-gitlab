# Projects API

## List projects

Get a list of visible projects for authenticated user. When accessed without authentication, only public projects are returned.

```javascript
let projects = GitlabAPI.projects.all();
```

Parameters: [List all projects](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#list-projects)


### Get single project

Get a specific project. This endpoint can be accessed without authentication if
the project is publicly accessible.

```javascript
// From a project ID
let projectA = GitlabAPI.projects.show(21);

// From a projects url
let projectB = GitlabAPI.projects.show('diaspora/diaspora');
```

Parameters: [Get single project](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#get-single-project)


### Create project

Creates a new project owned by the authenticated user.

```javascript
// From a project ID
let projectA = GitlabAPI.projects.create({
  // params
});
```
Parameters: [Create project](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#create-project)


### Create project for user

Creates a new project owned by the specified user. Available only for admins.

```javascript
// From a project ID
let projectA = GitlabAPI.projects.createForUser(userId, {
  // params
});
```
Parameters: [Create project for user](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#create-project-for-user)


### Edit project

Creates a new project owned by the specified user. Available only for admins.

```javascript
// From a project ID
let projectA = GitlabAPI.projects.edit(projectId, {
  // params
});
```
Parameters: [Edit project](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#edit-project)


### Fork project

Forks a project into the user namespace of the authenticated user or the one provided.

```javascript
// From a project ID
let projectA = GitlabAPI.projects.fork(projectId, {
  // params
});
```
Parameters: [Fork project](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md#fork-project)