---
sidebar_position: 1
---

# Resource Controller

The resource controller handles all requests related to resources, including uploading, updating, and deleting resources, as well as loading resources for display. The resources have a mongo model and are stored in AWS.

## Functions Explanations

### uploadResource

Handles the uploading of a new resource. It creates a new Resource object with the provided information and saves it to the database.

### updateResource

Updates an existing resource with new information. It finds the resource by ID, modifies its properties, and saves the changes.

### postPublicResource

Changes the status of a resource to "finalPublic," indicating that it is publicly available.

### removePublicResource

Changes the status of a resource back to "public," removing its public availability.

### removeResource

Deletes a resource from the database.

### uploadToPublicResr

Handles the uploading of a new resource to the public resources section. It creates a new Resource object with the provided information, sets the status to "approve," and saves it to the database.

### updateOwner

Updates the owner of a resource. It finds the resource by ID, modifies the owner ID and owner name, and saves the changes.

### getCurrentOwner

Retrieves the current owner of a resource.

### loadResources

Loads resources for a specific course. It retrieves resources based on the course ID and check status, sorts them by creation date, and limits the number of resources to load.

### loadMoreResourcesAjax

Loads more resources for a specific course using AJAX. It retrieves additional resources based on the skip value and sends them as a response.

### addAuthor

A helper function that adds authors' names to the resource object.

### loadAllFacultyResources

Loads resources related to faculty members. It retrieves syllabus, assignments, and guides resources, limited to three each.

### loadImpactResources

Loads resources related to faculty research and essays about ENACT.

### loadSpecificContentType

Loads resources of a specific content type, such as syllabus, assignments, faculty research, essay ENACT, or course planning.

### loadImages

Loads image paths for slideshow, faculty, and label images.

### loadPublicResources

Loads all public resources available.

### loadDisplayedResources

Loads publicly displayed resources.

### showMyResources

Shows the resources owned by the currently logged-in user.

### getTags(req, res)

This async function retrieves a list of predefined tags and approved tags from the database.

### showPublic(req, res, next)

This async function retrieves and renders the information of public resources to be displayed on a page.

### starResource(req, res, next)

This async function handles the process of marking a resource as a favorite by adding its ID to the user's favorite resource set in the database.

### unstarResource(req, res, next)

This async function handles the process of removing a resource from the user's favorite resource set in the database.

### showStarredResources(req, res, next)

This async function retrieves and renders the information of resources that have been marked as favorites by the user.

### loadCollection(req, res, next)

This async function retrieves and loads the resources belonging to a specific resource set (collection) for display.

### removeFromCollection(req, res, next)

This async function handles the process of removing a resource from a resource set (collection) in the database.

### addToCollection(req, res, next)

This async function handles the process of adding a resource to a resource set (collection) in the database.

### createCollection(req, res, next)

This async function creates a new resource set (collection) in the database with the provided collection name.

### deleteCollection(req, res, next)

This async function deletes a resource set (collection) from the database.

### primarySearch(req, res, next)

This async function performs a primary search operation based on the user's input and renders the search results.

### invertedSearch(req, res)

This async function performs an inverted search operation based on the user's input and returns the search results.

### advancedSearch(req, res)

This async function performs an advanced search operation based on the user's input and filters the search results accordingly.

### advancedSearchPublic(req, res)

This async function performs an advanced search operation for public users based on the user's input and filters the search results accordingly.

### getAllResourcesAjax(req, res)

This async function retrieves all resources from the database and returns them as a response in an Ajax request.
