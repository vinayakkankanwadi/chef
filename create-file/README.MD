
Create file using chef
---

Step 1
---
create cookbooks folder

```
mkdir cookbooks
```

Step 2
---
create create-file folder

```
cd cookbooks
mkdir create-file
```

Step 3
---
create recepies folder

```
cd create-file
mkdir recipes
```

Step 4
---
create default.rb recipe file

```
cd recipes
notepad default.rb
```

Step 5
---
Update the content of default.rb to create file

```
file 'c:\users\<username>\desktop\hello.txt' do
  content 'Welcome to Chef'
end
```

Step 6
---
Run the chef locally

```
create-file> chef-client --local-mode --runlist 'recipe[create-file]'
```
