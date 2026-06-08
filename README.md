Git & Git Diff Complete Cheat Sheet 🚀

Git me jab bhi aap kaam karte ho, toh sabse bada sawal hota hai: "Maine pichli baar se abhi tak code me kya badlaa hai?" Is sawal ka jawab dene ke liye git diff sabse behtareen command hai.

1. Git ke 4 Main Areas (Samajhna Jaroori Hai)

Git me aapka code hamesha in 4 states/areas me se kisi ek me hota hai:

Working Directory (WD): Aapka local folder jahan aap abhi code likh rahe ho (untracked ya modified files).

Staging Area (Index): git add . karne ke baad code yahan jata hai. Ye commit hone ki taiyari hai.

Local Repository (HEAD): git commit karne ke baad aapka code local system me permanently save ho jata hai.

Remote Repository (GitHub): git push karne ke baad code GitHub par chala jata hai.

2. Git Diff Commands Cheat Sheet

Command

Kya Karti Hai? (Purpose)

Kab Use Karein?

git diff

Working Directory aur Staging Area ke beech ka difference dikhati hai.

git add karne se pehle badlav check karne ke liye.

git diff <filename>

Kisi ek specific file me hue badlav ko dekhne ke liye.

Jab sirf ek file check karni ho.

git diff HEAD

Working Directory aur aakhri commit ke beech ka difference.

git add kiya ho ya nahi, sab badlav dekhne ke liye.

git diff --staged

Staging Area aur aakhri commit ke beech ka difference.

git commit karne se pehle double check karne ke liye.

git diff <commit1> <commit2>

Do alag-alag commits ke beech ka difference dekhne ke liye.

Purane badlav ko naye badlav se compare karne ke liye.

git diff <branch1> <branch2>

Do alag branches ke beech ka difference dekhne ke liye.

Merge karne se pehle dono branches ka code compare karne ke liye.

3. Practical Examples (Kaise Use Karein)

A. Working Directory vs Staging Area

Aapne file me badlav kiya, par abhi git add nahi kiya hai:

git diff README.md


B. Staging Area vs Last Commit (HEAD)

Aapne git add . kar diya hai, par abhi commit baki hai. Aap dekhna chahte ho ki commit me kya-kya ja raha hai:

git diff --staged
# ya fir
git diff --cached


C. Working Directory vs Last Commit

Aapne jo bhi badlav kiye hain (chahe add kiya ho ya na kiya ho), use seedhe pichle commit se compare karein:

git diff HEAD README.md


D. Do Commits ke Beech ka Antar

Agar aapko do purane commits ke beech ka difference dekhna hai (Commit IDs git log --oneline se milegi):

git diff abc1234 xyz5678


E. Apne local code ko GitHub ke code se compare karna

git diff main origin/main


4. Git Diff ke Output ko Kaise Padhein? (How to Read)

Jab aap git diff chalate ho, toh terminal me kuch aisi lines dikhti hain:

🟢 + (Plus sign) in Green: Iska matlab ye line nayee add ki gayi hai.

🔴 - (Minus sign) in Red: Iska matlab ye line purani file se delete (remove) kar di gayi hai.

⚪ Plain text (No sign): Ye lines unchanged hain (sirf context dene ke liye dikhayi jati hain).

5. Quick Workflow Tip for DevOps 💡

Jab bhi aap kisi project me kaam kar rahe ho, toh push karne se pehle ye workflow hamesha follow karein:

git status (Check karein kaunsi files modify hui hain).

git diff (Apne saare badlav ko dhyan se verify karein taaki koi galti na ho).

git add . (Files ko stage karein).

git diff --staged (Commit karne se pehle aakhri baar check karein).

git commit -m "aapka message" (Commit karein).

git push origin main (GitHub par push karein).
