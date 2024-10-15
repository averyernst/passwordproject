# Author: Avery Ernst
# Email: amernst@umass.edu
# SPIRE ID: 34605274

list_of_words=["abruptly","affix","axiom","bagpipes","banjo","bikini",
               "buckaroo","buxom","curacao","dirndl","dizzying","dwarves",
               "embezzle","fishhook","espionage","fjord","fuchsia",
               "galaxy","gazebo","gizmo","gnarly","haiku","hyphen",
               "icebox","jaundice","jaywalk","jazzy","juicy","kazoo",
               "kilobyte","kiosk","lucky","matrix","marquis","mnemonic",
               "nowadays","onyx","oxidize","peekaboo","pixel","polka",
               "quizzes","quorum","rhubarb","snazzy","squawk","sphinx",
               "stretch","subway","thumbscrew","topaz","twelfth",
               "unworthy","unzip","unzip","vodka","vortex","waltz",
               "wavy","wheezy","whomever","wizard","yolk","zodiac"]
import random
chooseword=random.choice(list_of_words)

def the_man(incorrectguess):
    if incorrectguess==0:
        print("      +━━━━+")
        print("      ┃")
        print("      ┃")
        print("      ┃")
        print("     ───")
    elif incorrectguess==1:
        print("      +━━━━+")
        print("      ┃    O")
        print("      ┃")
        print("      ┃")
        print("     ───")
        
print(the_man(0))
