# Quick example on scanning directory and get files in it

The goal is to scan the directory, see if there's any `json` file, then `deserialize` those file into `Character` object.

First we create a `DirectoryInfo` object.

Second we assign `DirectoryInfo.GetFiles("*.json");` into `FileInfo` object. This acts like an array contains all the file `FileInfo` objects.

Then we loop through the `FileInfo` object we create earlier, `File.ReadAllText` and `JsonSerializer.Deserialize` them

# IMPORTANT: You need a default constructor for the `JsonSerializer.Deserialize` to work, else it returns `exception` for some reason
