Git Guidelines
==============

- Follow this basic template:
    > **Title**  
    > Should be a single sentence, no period at the end  
    > Should make the assumption of starting [this commit should], so no conjugation. For instance, [this commit should] **Make** something work  
    > <br/>
    > **Description**  
    > Use sentences, or `*` for list  
    > <br/>
    > **re #[number of related ticket]**
- Break commits by context (client, server, etc) and features.
- Use `git commit --fixup [commit hash]` when fixing something related to a previous commit.
- You should not start commits with "Implement + [verb]", just "[verb] ..." is enough.
- You should not put everything in a huge commit.
- When squashing commits do:
    > git checkout -b temp
    > git checkout currentBranch
    > git rebase -i ... [--autosquash]
    > git diff temp
