1. >>> cat clean_dialog.csv | wc -l
>>> 36860
- The dataset is 36860 lines long.

2. >>> head clean_dialog.csv
>>> "title","writer","pony","dialog"
"Friendship is Magic, part 1","Lauren Faust","Narrator","Once upon a time, in the magical land of Equestria, there were two regal sisters who ruled together..."
- The fields are title, writer, pony, dialog, and they contain the episode title and part, the writer of the episode, the pony or character speaking, and the dialog that they say. 

3. >>> cut -d',' -f1 clean_dialog.csv | tail -n +2 | sort | uniq | wc -l
>>> 196
- It covers 196 episodes. 

4. >>> head clean_dialog.csv
>>> >>> "title","writer","pony","dialog"
"Friendship is Magic, part 1","Lauren Faust","Narrator","Once upon a time, in the magical land of Equestria, there were two regal sisters who ruled together..."
- One unexpected is that not each line value under "pony" is actually a pony, for example the first person to speak is the Narrator, who may or may not be counted as a pony downstream in the analysis. 