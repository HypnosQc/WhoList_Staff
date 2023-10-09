
# Latest AzerothCore Revision 2023/10/08 MiscHandler.cpp File


# WhoList_Staff
Azerothcore Edit that show Staff rank in Who List
Credits to [Revision - noisiver] Revision#2262 (Help on the script) / [Trojan] Trojan#1312 (Help & Fix on the script) & [Dandi] Dandi#2828 (Help & Fix on the script + Making it to work with the final touch)


Just Download the "MiscHandler.cpp" & put it in your Source Folder
...src\server\game\Handlers

 or

 ****Copy the Code line & put them at line 398 of "MiscHandler.cpp".*****
****Remove the line 398 by Pasting the code on it****

Line 398 in MiscHandler.cpp
****data << target.GetPlayerName();                   // player name**** 



****Code to Paste On line 398****
std::string playerName = ""; //temp storage

        //definition of playerName depending on the (player/GM)'s rank
        if (target.GetSecurity() >= 1) //if the rank is 1 or above
            playerName = "|cffFFFFFF[|r|cffFA8258Staff|cffffffff]|r  " + target.GetPlayerName();
        else
            playerName = target.GetPlayerName();

        
        data << playerName;                               //player name - with Staff indicator
      //data << target.GetPlayerName();                 // player name - commented out to be replaced with the new playerName



