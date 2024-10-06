## TMUX Logging Manager
```shell-session
$ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
```shell-session
$ touch .tmux.conf
```
```shell-session
$ cat .tmux.conf 
```
```shell-session
$ tmux source ~/.tmux.conf 
```
Next, we can start a new Tmux session (i.e., `tmux new -s setup`).

Once in the session, type `[Ctrl] + [B]` and then hit `[Shift] + [I]` (or `prefix` + `[Shift] + [I]` if you are not using the default prefix key), and the plugin will install (this could take around 5 seconds to complete).

Once the plugin is installed, start logging the current session (or pane) by typing `[Ctrl] + [B]` followed by `[Shift] + [P]` (`prefix` + `[Shift] + [P]`) to begin logging. If all went as planned, the bottom of the window will show that logging is enabled and the output file. To stop logging, repeat the `prefix` + `[Shift] + [P]` key combo or type `exit` to kill the session. Note that the log file will only be populated once you either stop logging or exit the Tmux session.

If we forget to enable Tmux logging and are deep into a project, we can perform retroactive logging by typing `[Ctrl] + [B]` and then hitting `[Alt] + [Shift] + [P]` (`prefix` + `[Alt] + [Shift] + [P]`), and the entire pane will be saved. The amount of saved data depends on the Tmux `history-limit` or the number of lines kept in the Tmux scrollback buffer. If this is left at the default value and we try to perform retroactive logging, we will most likely lose data from earlier in the assessment. To safeguard against this situation, we can add the following lines to the `.tmux.conf` file (adjusting the number of lines as we please):

#### Tmux.conf
```shell-session
set -g history-limit 50000
```
Another handy trick is the ability to take a screen capture of the current Tmux window or an individual pane. Let's say we are working with a split window (2 panes), one with `Responder` and one with `ntlmrelayx.py`. If we attempt to copy/paste the output from one pane, we will grab data from the other pane along with it, which will look very messy and require cleanup. We can avoid this by taking a screen capture as follows: `[Ctrl] + [B]` followed by `[Alt] + [P]` (`prefix` + `[Alt] + [P]`). Let's see a quick demo.

To recreate the above example first start a new tmux session: `tmux new -s sessionname`. Once in the session type `[Ctrl] + [B]` + `[Shift] + [%]` (`prefix` + `[Shift] + [%]`) to split the panes vertically (replace the `[%]` with `["]` to do a horizontal split). We can then move from pane to pane by typing `[Ctrl] + [B]` + `[O]` (`prefix` + `[O]`).

Finally, we can clear the pane history by typing `[Ctrl] + [B]` followed by `[Alt] + [C]` (`prefix` + `[Alt] + [C]`).

```shell-session
$ mkdir -p ACME-IPT/{Admin,Deliverables,Evidence/{Findings,Scans/{Vuln,Service,Web,'AD Enumeration'},Notes,OSINT,Wireless,'Logging output','Misc Files'},Retest}
```