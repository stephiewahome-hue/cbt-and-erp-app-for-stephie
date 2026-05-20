# cbt-and-erp-app-for-stephie
im creating an app to monitor mdd and ocd and other mental illnesses
We are going to build this entire full-stack application completely from scratch, step-by-step. Because we want this to be a beautiful, production-ready project for your GitHub portfolio, we will use Next.js (React), TypeScript, TailwindCSS, and Prisma with SQLite so your data is securely saved on your computer and never forgotten.

🛠️ The Architecture & Setup Blueprint
First, let's look at how the entire system connects. This visual chart shows exactly how your frontend screens talk to your backend server database without using any labels.
## System Architecture

```text
+---------------------------------------+
|         CLIENT (Next.js Frontend)     |
|   React Components + Tailwind UI      |
+-------------------+-------------------+
                    |
        POST / GET (JSON Payload)
                    |
+-------------------v-------------------+
|          SERVER (Next.js API Routes)  |
|   Prisma Client / Controller Filters  |
+-------------------+-------------------+
                    |
             Object Mapping
                    |
+-------------------v-------------------+
|         DATABASE (Local SQLite)       |
|   Isolated, Encrypted relational tables|
+---------------------------------------+
Initial Terminal Setup
 Go to your local storage or browser and install node.js and give permissions to windows shell,Open your machine's terminal which is windows powers shell , find your working directory, and run these commands to generate the codebase and install your icons and database tools:
Install globally once:
npm install -g create-next-app
Then you can run:
create-next-app mind-console --typescript --tailwind --app --src-dir=false --yes
without waiting for npx to fetch it each time.
Use npm cache  
Make sure your npm cache is healthy:
npm cache verify
Run only once  
After the project is created, you don’t need to rerun npx create-next-app. Just cd into the folder and continue with dependency installs.
cd mind-console
npm install lucide-react @prisma/client
npm install prisma --save-dev
npx prisma init --datasource-provider sqlite



