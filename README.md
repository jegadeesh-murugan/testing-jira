# testing-jira

This repository will be used to validate the integration between Jira and GitHub.

## Goal
Verify that Jira issues and GitHub activities are connected end to end, including issue linking, status updates, and workflow visibility.

## Test Scope
- Create a Jira issue and link it to a GitHub branch or pull request.
- Verify that commits and pull requests reference the Jira issue key correctly.
- Confirm that GitHub actions or deployments can post status updates back to Jira.
- Validate that comments or workflow transitions are reflected in the connected tools.

## Prerequisites
- A Jira project with webhook or integration support enabled.
- A GitHub repository with access to the required integration app or token.
- A test issue key such as TEST-123.
- A branch naming convention that includes the Jira issue key.

## Test Cases
1. Branch to Jira link
   - Create a branch named `TEST-123-test-integration`.
   - Confirm the branch is visible in Jira and linked to the issue.

2. Commit reference
   - Add a commit message containing `TEST-123`.
   - Verify that the commit appears in Jira under the related issue activity.

3. Pull request workflow
   - Open a pull request from the test branch.
   - Confirm that the PR is linked to the Jira issue and that status updates are visible.

4. Status update flow
   - Merge or update the pull request state.
   - Verify that the Jira issue reflects the latest development status.

5. Comment and notification checks
   - Add comments in GitHub or Jira.
   - Confirm that notifications or comments are propagated according to the configured integration rules.

## Expected Outcome
The Jira issue should show clear evidence of linked GitHub activity, and GitHub should be able to reference and update the Jira issue in a consistent way.

## Verification Evidence
- Branch checked: TEST-123-test-in
- Latest commit: TEST-123 add integration test note
- Pull request: https://github.com/jegadeesh-murugan/testing-jira/pull/1
- PR state: OPEN

Integration test note
