# junit-report-slack
Github action to notify JUnit test results via Slack

## Objective
The objective of this action is to publish the Junit test results summary as part of a Slack message.

## Message Details
JUnit test result xml file contains test suite information with total tests, failed and skipped test count. This action parses the xml report, generates a message like below and posts the message to the given slack channel.
### Message Format
- Title: Test Run Title ( needs to pass as a parameter)
- Total: Count of total test cases in the suite
- Passed: Count of total passed test cases.
- Failed: Count of failed test cases.
- Skipped: Count of skipped test cases.
### Message Screenshot
![image](https://github.com/qafficient/junit-report-slack/assets/58494847/494195b0-7d7d-4d57-b835-2a41c740090e)

## How to use?
```
- name: Junit report in Slack
  if: always()
  uses: qafficient/junit-report-slack@v1.0.3
  with:
    testRunName: <Test Report Name>
    slackToken: <slack api token>
    slackChannelId: <slack channel id>
    testOutputPath: <JUnit test report xml full file path>
```
## License
The scripts and documentation in this project are released under the [MIT License](https://github.com/qafficient/junit-report-slack/blob/update-readme/LICENSE)

