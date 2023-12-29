The {% data variables.dependency-review.action_name %} scans your pull requests for dependency changes and raises an error if any new dependencies have known vulnerabilities.{% ifversion fpt or ghec or ghes %} The action is supported by an API endpoint that compares the dependencies between two revisions and reports any differences.{% endif %}

For more information about the action{% ifversion fpt or ghec or ghes %} and the API endpoint{% endif %}, see the [`dependency-review-action`](https://github.com/actions/dependency-review-action) documentation{% ifversion fpt or ghec or ghes %}, and "[AUTOTITLE](/rest/dependency-graph/dependency-review)" in the API documentation.{% endif %}