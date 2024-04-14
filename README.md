# ML.MD

This repository is a machine learning notebook developed in [Obsidian](https://www.obsidian.md).

# Setting up Quartz

## 1. Initialize quartz with 
```bash
npx quartz create
```

### 1.1. You are then asked to choose between three different methods of initializing the content in your directory: 
```
- Empty Quartz
- Copy an existing folder
- Symlink an existing folder
```
Select `Symlink an existing folder` and use the **full path** (i.e. `/home/ml.md`) to the Obsidian vault.

### 1.2. You should then see something like this:
```
Choose how Quartz should resolve links in your content. You can change this later in `quartz.config.ts`.
- Treat links as absolute path
- Treat links as shortest path
- Treat links as relative paths
```
What you select here is dependent on how you prefer to handle links in Obsidian. By default, Obsidian uses the shortest path where possible.

## 2. Sync the changes with 
```bash
npx quartz sync --no-pull
```
## 3. After all the changes have been done, sync them with 
```bash
npx quartz sync
```

# Updating Site with New Notes

In the folder `/home/ml.md` run
```bash
make public
```