# Testing

!SLIDE

# API Testing

- Successful Responses ("Happy Path :)")
- Error Codes and Messages ("Sad Path :(")

!SLIDE

# Testing Tools

- Shell scripts that call `curl` or `wget`
- Framework's native tests, eg. Rails integration tests
- Language-agnostic tools, eg. Postman GUI + Newman CLI

!SLIDE

# Rails: [Integration Tests](https://guides.rubyonrails.org/testing.html#integration-testing)

```ruby
test "should get /projects" do
  get v0_projects_url
  assert_response :success # 200
end

test "/projects should get list of projects" do
  get v0_projects_url
  assert_equal config_projects.to_json(), @response.body
end

test "/projects/:projectId should return a 404 if project is not found" do
  project_name = 'unknownProjectX'
  get v0_project_url(project_name)
  assert_response :missing # 404
  response_body = JSON.parse @response.body
  assert_equal 'Project Not Found', response_body['error']['name']
  assert_equal "Unable to find project '#{project_name}'", response_body['error']['message']
end
```

!SLIDE

# Postman GUI + newman CLI

Tests configured in JSON and written in ChaiJS

Tests performed against running API server

![](images/postman.png)
