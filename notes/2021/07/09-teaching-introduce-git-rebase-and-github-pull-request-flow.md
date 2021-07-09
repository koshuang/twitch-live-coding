# 2021-07-09 Twitch Streaming

Subject: [Teaching] Introduce Git rebase and github pull request flow

<!--  
const div = document.querySelector('.sc-AxjAm .iltvOi');
div.innerText = 'https://hackmd.io/@koshuang/twitch-streaming';
div.style.fontSize='18px';
-->

## Agenda

- Remove usePubSub

- Topics
  - git
    - commands
      - push -f: forced push
      - cherry-pick
      - rebase
        - 重點： commit 之間的 denpendency 如果越低，越容易調換順序, A -> B
        - rebase 過後， commit id 會被改掉
        - 不應該修改(rebase)在 master 上面已經 push 的 commits
          - 例外：你是一人專案，且確定不會有問題，rebase -> forced push
        - 通常會習慣對自己的 feature branch 去 rebase

## References

- https://www.conventionalcommits.org/
- https://backlog.com/git-tutorial/tw/stepup/stepup7_5.html













