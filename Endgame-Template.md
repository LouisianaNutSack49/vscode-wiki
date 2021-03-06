- *Month/Day* Code freeze for the endgame
- *Month/Day* [Endgame done](https://github.com/Microsoft/vscode/wiki/Development-Process#inside-an-iteration)
- *Month/Day* Expected release date (this may change)

> **Note:** The `Insiders` build needs to be in the wild for 24 hours before we can enter the last phase of the endgame.

##### Monday
- [ ] Run [OSS tool](https://github.com/microsoft/vscode-build-tools/tree/master/distro-tools) **endgame master**
- [ ] Code freeze at 5pm PT
- [ ] Ensure we have a green build on all platforms at 5pm PT
- [ ] Create test plan items following the template [here](https://github.com/microsoft/vscode/wiki/Writing-Test-Plan-Items) by 6pm PT
- [ ] Add verification-needed label to features needed testing and are not tested by TPIs.
- [ ] Update your availability for testing here - https://vscode-tools.azurewebsites.net/

##### Tuesday
- [ ] Test plan items assigned (using https://vscode-tools.azurewebsites.net/)
  - Run the tool multiple times to balance load if test items come in later and assignments are already made
  - [Assigned to you](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+assignee%3A%40me++label%3Atestplan-item+)
- [ ] [🔖All closed feature-requests](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+archived%3Afalse+milestone%3A%22September+2019%22+user%3Amicrosoft+label%3Afeature-request+-label%3Averification-needed+-label%3Aon-testplan+-label%3Averified+-label%3A*duplicate+sort%3Aupdated-desc+) either have a `verification-needed` or `on-testplan` label
- [ ] Test build starts at 7am CET
- [ ] Test plan ready by 8am CET
- [ ] [🔖Testing](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+archived%3Afalse+label%3Atestplan-item+user%3Amicrosoft)
- [ ] [🔖Verification needed](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+archived%3Afalse+milestone%3A%22September+2019%22+user%3Amicrosoft+label%3Averification-needed+-label%3Averified)

##### Wednesday
- [ ] [🔖Testing](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+archived%3Afalse+label%3Atestplan-item+user%3Amicrosoft)
- [ ] Remind team members to assign issues that they intend to fix to the current milestone
- [ ] Fixing (self-assigned, milestone assigned)
- [ ] [🔖Verification needed](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+archived%3Afalse+milestone%3A%22September+2019%22+user%3Amicrosoft+label%3Averification-needed+-label%3Averified)

##### Thursday
- [ ] Fixing (scrutiny sets in - major bugs only - to be discussed in stand-up meeting, labeled as `candidate`)
- [ ] [🔖Verification needed](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+archived%3Afalse+milestone%3A%22September+2019%22+user%3Amicrosoft+label%3Averification-needed+-label%3Averified)
- [ ] [🔖Verification](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aclosed+is%3Aissue+user%3Amicrosoft+milestone%3A%22September+2019%22+label%3Abug+-label%3Averified+-label%3Aon-testplan+-label%3Aduplicate+-label%3A*duplicate+-label%3Ainvalid+-label%3Aas-designed+-label%3Aerror-telemetry+-repo%3Amicrosoft%2FAL+)

##### Friday
- [ ] Pause scheduled `insider` builds **endgame master**
- Satellite modules/npm packages ready, version updated, smoke tested
  - [ ] vscode **@bpasero**
  - [ ] yo generator **@aeschli**
  - [ ] vsce **@joaomoreno**
  - [ ] node debug **@weinand**
  - [ ] node debug2 **@roblourens**
  - [ ] node debugadapter node **@weinand**
- [ ] All issues [🔖verified](https://github.com/Microsoft/vscode/issues?q=is%3Aissue+label%3Abug+-label%3Averified+-label%3Aon-testplan+is%3Aclosed+-label%3Aduplicate+-label%3A%2Aduplicate+-label%3Ainvalid+-label%3Aas-designed+-label%3Aerror-telemetry+milestone%3A%22September+2019%22)
- [ ] Fixing (only critical bugs - no string changes)
- [Smoketest](https://github.com/Microsoft/vscode/wiki/Smoke-Test) (⚠️ MUST run with `--stable-build` argument ⚠️ )
  - [ ] Windows - **owner**
  - [ ] OS X - **owner**
  - [ ] Linux - **owner**
  - [ ] Web (manual until https://github.com/microsoft/vscode/issues/80308 is done) - **owner**
- [ ] All release notes updated
  - release notes are collected in a file named *`Month_Year.md`* in this [repo directory](https://github.com/Microsoft/vscode-docs/blob/vnext/release-notes/)
  - [ ] @aeschli
  - [ ] @alexdima
  - [ ] @alexr00
  - [ ] @bpasero
  - [ ] @chrmarti
  - [ ] @dbaeumer
  - [ ] @egamma
  - [ ] @isidorn
  - [ ] @joaomoreno
  - [ ] @jrieken
  - [ ] @kieferrm
  - [ ] @mjbvz
  - [ ] @octref
  - [ ] @rebornix
  - [ ] @rmacfarlane
  - [ ] @roblourens
  - [ ] @sandy081
  - [ ] @sbatten
  - [ ] @tyriar
  - [ ] @weinand
- [ ] Acknowledge pull requests in release notes. We acknowledge PRs from outside the team. Use the [thankyou](https://vscode-tools.azurewebsites.net/#acknowledgePRs) tool to generate the initial contents of the section. **owner**
  - [ ] vscode **endgame master**
  - [ ] vscode-node-debug **@weinand**
  - [ ] vscode-node-debug2 **@roblourens**
  - [ ] vscode-debugadapter-node **@weinand**
  - [ ] vscode-js-debug **@connor4312**
  - [ ] vscode-languageserver-node **@dbaeumer**
  - [ ] language-server-protocol **@dbaeumer**
  - [ ] vscode-textmate **@alexdima**
  - [ ] vscode-loader **@alexdima**
  - [ ] vscode-generator-code **@aeschli**
  - [ ] vscode-vsce **@joaomoreno**
  - [ ] vscode-docs **@gregvanl**
  - [ ] vscode-css-languageservice **@aeschli**
  - [ ] vscode-json-languageservice **@aeschli**
  - [ ] vscode-html-languageservice **@aeschli**
  - [ ] jsonc-parser **@aeschli**
  - [ ] vscode-tslint **@egamma**
  - [ ] vscode-eslint **@dbaeumer**
  - [ ] vscode-jshint **@rmacfarlane**
  - [ ] vscode-recipes **@chrisdias**
  - [ ] localization **@weeteckt**
  - [ ] vscode-github-issues-prs **@chrmarti**
  - [ ] inno-updater **@joaomoreno**
- [ ] Review pull requests acknowledgements with `NOT MERGED - PLS REVIEW`. **endgame master**
- [ ] Acknowledge issue trackers from the community **@chrmarti**
- [ ] Add notable fixes to the release notes **all**
- When done fixing/verifying and there are changes since last build at the end of day PT
  - [ ] Trigger new insider build and publish it manually **endgame master**

##### Friday/Monday
- [ ] Branch code to `release/<x.y> **endgame master**
- [ ] Bump up the version in package.json - **endgame master**
- [ ] Announce master is open for business **endgame master**
- [ ] Polish release notes **redmond**

##### Monday - Wednesday
- [ ] [🔖milestone issues](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+user%3Amicrosoft+milestone%3A%22September+2019%22)
- [ ] [🔖candidate issues](https://github.com/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+user%3Amicrosoft+label%3Acandidate)
- [ ] Polish release notes **redmond**
- [ ] Cherry-pick hand-picked and reviewed changes to `release/<x.y>` **endgame master**
- [ ] Build `Insider` from `release/<x.y>` **endgame master**
- [ ] Manually release `Insider` **endgame master**
- [ ] Build stable for all platforms as new candidate issues come in **endgame master**
- [ ] Documentation updated
  - [ ] @aeschli
  - [ ] @alexdima
  - [ ] @alexr00
  - [ ] @bpasero
  - [ ] @chrmarti
  - [ ] @dbaeumer
  - [ ] @egamma
  - [ ] @isidorn
  - [ ] @joaomoreno
  - [ ] @jrieken
  - [ ] @kieferrm
  - [ ] @mjbvz
  - [ ] @octref
  - [ ] @rebornix
  - [ ] @rmacfarlane
  - [ ] @roblourens
  - [ ] @sandy081
  - [ ] @sbatten
  - [ ] @tyriar
  - [ ] @weinand
- [ ] Run `scripts/test-documentation.sh|bat` and add file or fix issues if there are new colors that are not documented.

> **Note:** The `Insiders` build needs to be in the wild for 24 hours before we can enter the last phase of the endgame. **endgame master**

##### Wednesday/Thursday
- [ ] Build stable for all platforms **endgame master**
- [ ] Sanity check of installable bits
  - [ ] Windows 32 bit **owner**
    - [ ] signed installer 32-bit
    - [ ] signed user installer 32-bit
    - [ ] zip 32-bit
  - [ ] Windows 64 bit **owner**
    - [ ] signed installer 64-bit
    - [ ] signed user installer 64-bit
    - [ ] zip 64-bit
  - [ ] OS X - **owner**
  - [ ] Linux
    - [ ] deb package 64-bit **owner**
    - [ ] rpm package 64-bit **owner**
    - [ ] archives **owner**
  - [ ] Server ([instructions](https://github.com/microsoft/vscode-remote-release/wiki/Sanity-Check-VS-Code-Servers)) **owner**
- [ ] Publish website **@gregvanl**
- [ ] Publish Localization language pack **@weeteckt**
- [ ] Publish to stable **endgame master**
- [ ] Add a git tag to `HEAD` of `release/<x.y>` in format `x.y.z` (for vscode.d.ts download)  **endgame master**
- [ ] [Publish @types/vscode](https://github.com/microsoft/vscode/wiki/Publish-vscode-types) **endgame master**
- [ ] Enable scheduled `insider` builds **endgame master**
- [ ] Twitter announcement **@chrisdias**
