# Using the Prompt Symlink Script

The `copy_prompts.ps1` script allows you to create symbolic links from multiple projects to a single set of prompt files, ensuring all projects use the latest prompts.

## Prerequisites
- Windows PowerShell
- Administrator privileges

## Usage
1. Create a text file with the paths to your target projects, one per line:
   ```
   C:\Projects\gamedev\Fractavere
   C:\Projects\ai\software_prompt_engineering
   C:\Projects\ai\coding_tools
   ```

2. Run PowerShell as Administrator (right-click PowerShell and select "Run as Administrator")

3. Execute the script with:
   ```
   .\create_symlink_for_prompts.ps1 -PathsFile project_paths.txt
   ```

This will create symbolic links in all target projects pointing to the `.cursor\rules\global_prompts` directory in the current project. When you update prompts in the current project, all linked projects will automatically use the updated versions.

# TODO
- When creating new files, automatically make a new class for the contents inside that file
- Optimize docstring generation for the new files, especially that they are classes now, and the prompt is missing instructions for those
- Automatic integration with the Cursor Agent feature to for example: write the requirements.txt file automatically
