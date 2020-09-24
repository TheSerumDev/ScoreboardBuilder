# ScoreboardBuilder
Scoreboard Builder for spigot

**INFORMATION** <br />-----------------<br />
The library is currently in the **BETA-Phase!**<br /> Errors can happen, so if you found a bug, please let me know. You can contact me at the email address **scoreboard-library@serumdev.de**; or via Twitter at https://www.twitter.com/SerumDev via Direct Message. Thanks!

# How to work with this library?

#### plugin.yml:
name: ScoreboardTestPlugin<br />
author: SerumDev<br />
version: 1.0<br />
main: de.serumdev.scoreboardtestplugin.ScoreboardTestPlugin<br /><br />
depend: [ScoreboardApi]<br /><br />
api-version 1.16<br /><br />
commands:<br />

#### Example Main Class:

#### Let's start with the implementation of the API, so that we can access the methods of the API later

```java 
public class ScoreboardTestPlugin extends JavaPlugin {
  private static ScoreboardTestPlugin instance;
  private ScoreboardApi scoreboardApi;

  @Override
  public void onLoad() {
    instance = this;
  }

  @Override
  public void onEnable() {
    init();
  }

  @Override
  public void onDisable() {

  }

  private void init() {
    this.scoreboardApi = (ScoreboardApi) Bukkit.getPluginManager().getPlugin("ScoreboardApi");
  }

  public static ScoreboardTestPlugin getInstance() {
    return instance;
  }

  public ScoreboardApi getScoreboardApi() {
    return scoreboardApi;
  }
}
```

# Introduction to the methods:
 ## ScoreBoardManager:
 #### getScoreboard(Player p, Consumer<Scoreboard> callback); 
