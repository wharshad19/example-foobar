Code Climate Lunch & Learn Example



Example files: https://gist.github.com/dblandin/589e70345774298e1622850349c31876

## Setup

1. Install the Code Climate [browser extension](https://codeclimate.com/browser-extension)
2. [Fork](https://github.com/davehenton/example-foobar) this project to your own GitHub user. 
3. Import your new fork of the repo to Quality, using the `Open Source` section of the Quality UI.
4. Update the included CircleCI config file with the Test Reporter ID found in your Repo Settings in Quality.
5. Create a CircleCI user, and add your repo to CircleCI. 
6. Head back to the Quality UI, and install the GitHub PR Integration for your repo. 



## Introduce some complexity

1. In the GitHub UI, modify `foo_bar.rb` with [this content](https://gist.github.com/dblandin/589e70345774298e1622850349c31876#file-foo_bar-rb) from gist
2. When committing the changes, create a new branch titled `demo-branch` for the commit and start a pull request. 


You should now see a Cognitive Complexity issue reported by Code Climate as a PR status
and via the browser extension. Test coverage reporting should also show
uncovered lines via the browser extension and a drop in coverage via the `diff-coverage` and `total-coverage` statuses.

<img src="https://raw.githubusercontent.com/codeclimate-demo/example-foobar/master/screenshots/2017-05-23-053352_1542x769_scrot.png" align="center" width="600" />

<img src="https://raw.githubusercontent.com/codeclimate-demo/example-foobar/master/screenshots/2017-05-23-053406_1810x1125_scrot.png" align="center" width="600" />

## Add some test coverage

1. Create a CircleCI user and add your repo via the CircleUI UI. 
2. Update your repo's CircleCI config file (on your master branch) with your repo's Test Reporter ID. Commit the update to master without opening a pull request. The Test Reporter ID is found in the Repo Settings in the Quality UI.
3. On your existing `demo-branch` branch, modify `spec/foo_bar_spec.rb` with [this content](https://gist.github.com/dblandin/589e70345774298e1622850349c31876#file-foo_bar_spec-rb) from gist
4. Commit the update to `demo-branch`. 

You should now see green annotations which show the lines that are now covered after you added those tests. 
<img src="https://raw.githubusercontent.com/codeclimate-demo/example-foobar/master/screenshots/2017-05-23-053507_2560x1415_scrot.png" align="center" width="600" />
<img src="https://raw.githubusercontent.com/codeclimate-demo/example-foobar/master/screenshots/2017-05-23-053532_1802x1070_scrot.png" align="center" width="600" />

## Introduce some duplication

1. Modify `duplication.rb` and `duplication_2.rb` with [these](https://gist.github.com/dblandin/589e70345774298e1622850349c31876#file-duplication-rb) [files](https://gist.github.com/dblandin/589e70345774298e1622850349c31876#file-duplication_2-rb)

1. Commit and push to your fork PR branch

    ```
    git add duplication.rb duplication_2.rb
    git commit -m "Add duplication"
    git push origin master
    ```

You should now see duplication issues reported by Code Climate.

<img src="https://raw.githubusercontent.com/codeclimate-demo/example-foobar/master/screenshots/2017-05-23-053732_1798x983_scrot.png" align="center" width="600" />
  
