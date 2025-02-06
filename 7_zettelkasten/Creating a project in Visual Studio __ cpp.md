# Meta
2025-02-02 12:32
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #pending 

# Creating a project in Visual Studio
Select *Create a new project* → *Windows Desktop Wizard* → click *Next*.

Name the project (i.e., ‘HelloWorld’), select location, and tick *Place solution and project in the same directory* → Click *Create*.

Under *Windows Desktop Project*, select *Console Application (.exe)* under Application type, and make sure *Precompiled Header* is **not selected**.

> [!info] **Q: What are precompiled headers and why are we turning them off?**
> In large projects (with many files), precompiled headers can improve compilation speed by avoiding some redundant compilation that tends to occur in larger projects.
> 
> However, they require extra work to use, and for small projects make little to no difference in compilation times.