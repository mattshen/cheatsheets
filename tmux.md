<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
  <head>
    <META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=utf-8">
  </head>
  <body>
    <h1>tmux &amp; screen cheat-sheet</h1>
    <div id="content">
    <!-- Begin Content Here /-->
    <!-- Originally composed on April 29th, 2009 at 14:35 /-->
    <!-- Original URL: http://www.dayid.org/os/notes/tm.html /-->
    <!-- Current URL: http://maleah.dayid.org/comp/tm.html /-->
      <h1>screen and tmux</h1>
      <p>A comparison of the features (or more-so just a table of notes for accessing some of those features) for <a href="http://www.gnu.org/software/screen/" target="_blank">GNU screen</a> and BSD-licensed <a href="https://tmux.github.io/" target="_blank">tmux</a>.</p>
      <table border="1">
        <tr>
          <td colspan="3">
            <p>The formatting here is simple enough to understand (I would hope). ^ means ctrl+, so ^x is ctrl+x. M- means meta (generally left-alt or escape)+, so M-x is left-alt+x</p>
            <p>It should be noted that this is no where near a full feature-set of either group. This - being a cheat-sheet - is just to point out the most very basic features to get you on the road.</p>
            <p>Trust the developers and manpage writers more than me. This document is originally from 2009 when tmux was still new - since then both of these programs have had many updates and features added (not all of which have been dutifully noted here).</p>
          </td>
        </tr>
        <tr><td><strong>Action</strong>                                             </td>
            <td><strong>tmux</strong>                                               </td>
            <td><strong>screen</strong>                                             </td>
        </tr>
        <tr><td>start a new session                                                 </td>
            <td>tmux <em>OR</em><br>tmux new <em>OR</em><br>tmux new-session        </td>
            <td>screen                                                              </td>
        </tr>
        <tr><td>re-attach a detached session                                        </td>
            <td>tmux attach <em>OR</em><br>tmux attach-session                      </td>
            <td>screen-r                                                            </td>
        </tr>
        <tr><td>re-attach an attached session (detaching it from elsewhere)         </td>
            <td>tmux attach -d <em>OR</em><br>tmux attach-session -d                </td>
            <td>screen -dr                                                          </td>
        </tr>
        <tr><td>re-attach an attached session (keeping it attached elsewhere)       </td>
            <td>tmux attach <em>OR</em><br>tmux attach-session                      </td>
            <td>screen -x                                                           </td>
        </tr>
        <tr><td>detach from currently attached session                              </td>
            <td>^b d <em>OR</em><br>^b :detach                                      </td>
            <td>^a ^d <em>OR</em><br>^a :detach                                     </td>
        </tr>
        <tr><td>rename-window to newname                                            </td>
            <td>^b , &lt;newname&gt; <em>OR</em><br>^b :rename-window &lt;newn&gt;  </td>
            <td>^a A &lt;newname&gt;                                                </td>
        </tr>
        <tr><td>list windows                                                        </td>
            <td>^b w                                                                </td>
            <td>^a w                                                                </td>
        </tr>
        <tr><td>list windows in chooseable menu                                     </td>
            <td>                                                                    </td>
            <td>^a "                                                                </td>
        </tr>
        <tr><td>go to window #                                                      </td>
            <td>^b #                                                                </td>
            <td>^a #                                                                </td>
        </tr>
        <tr><td>go to last-active window                                            </td>
            <td>^b l                                                                </td>
            <td>^a ^a                                                               </td>
        </tr>
        <tr><td>go to next window                                                   </td>
            <td>^b n                                                                </td>
            <td>^a n                                                                </td>
        </tr>
        <tr><td>go to previous window                                               </td>
            <td>^b p                                                                </td>
            <td>^a p                                                                </td>
        </tr>
        <tr><td>see keybindings                                                     </td>
            <td>^b ?                                                                </td>
            <td>^a ?                                                                </td>
        </tr>
        <tr><td>list sessions                                                       </td>
            <td>^b s <em>OR</em><br>tmux ls <em>OR</em><br>tmux list-sessions       </td>
            <td>screen -ls                                                          </td>
        </tr>
        <tr><td>toggle visual bell                                                  </td>
            <td>                                                                    </td>
            <td>^a ^g                                                               </td>
        </tr>
        <tr><td>create another window                                               </td>
            <td>^b c                                                                </td>
            <td>^a c                                                                </td>
        </tr>
        <tr><td>exit current shell/window                                           </td>
            <td>^d                                                                  </td>
            <td>^d                                                                  </td>
        </tr>
        <tr><td>split window/pane horizontally                                      </td>
            <td>^b "                                                                </td>
            <td>^a S                                                                </td>
        </tr>
        <tr><td>split window/pane vertically                                        </td>
            <td>^b %                                                                </td>
            <td>^a |                                                                </td>
        </tr>
        <tr><td>switch to other pane                                                </td>
            <td>^b o                                                                </td>
            <td>^a &lt;tab&gt;                                                      </td>
        </tr>
        <tr><td>kill the current pane                                               </td>
            <td>^b x <em>OR</em> (logout/^D)                                        </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>collapse the current pane/split (but leave processes running)       </td>
            <td>                                                                    </td>
            <td>^a X                                                                </td>
        </tr>
        <tr><td>cycle location of panes                                             </td>
            <td>^b ^o                                                               </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>swap current pane with previous                                     </td>
            <td>^b {                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>swap current pane with next                                         </td>
            <td>^b }                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>show time                                                           </td>
            <td>^b t                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>show numeric values of panes                                        </td>
            <td>^b q                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>toggle zoom-state of current pane (maximize/return current pane)    </td>
            <td>^b z                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>break the current pane out of its window (to form new window)       </td>
            <td>^b !                                                                </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>re-arrange current panels within same window (different layouts)    </td>
            <td>^b [space]                                                          </td>
            <td>                                                                    </td>
        </tr>
        <tr><td>Kill the current window (and all panes within)                      </td>
            <td>^b killw [target-window]                                            </td>
            <td>                                                                    </td>
        </tr>
      </table>
    </div>
    <div id='footer'>
      <span>Last Modified: 2017/01/11<br>
      URL: <a href="http://maleah.dayid.org/comp/tm.html">http://maleah.dayid.org/comp/tm.html</a><br>
      <a href="http://validator.w3.org/check?uri=referer" title="w3.org validator"><img src="http://www.w3.org/Icons/valid-html401" alt="Valid HTML 4.01 Transitional" height="31" width="88"></a>
      <a href="http://www.vim.org" title="vim.org"><img src="/icons/vi.gif" alt="Written in the vi editor" height="31" width="88"></a></span>
    </div>
  </body>
</html>

