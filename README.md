# Fun with Azure Maps

Display random locations on a map and try to find interesting shapes in them - for instance, Italy has the shape of a boot.

## Experimentation results

This project is an experimentation, within the [Azure Trial Hackathon on Dev.to](https://dev.to/devteam/hack-the-microsoft-azure-trial-on-dev-2ne5):
- Use *Azure maps* to display maps of random locations on the globe
- Use *Azure computer vision* to find interesting shapes in the maps

So far the experimentation did not go too well, not many discoveries made.

Some interesting insights however:
- when picking random map coordinates on the globe surface, most of the time the corresponding image is just blank (or blue or green or gray) and does not have much displayed
- to detect blank images, computing the standard deviation of all color channels works reasonably well
- there are some nice algorithms to compute the standard deviation efficiently, should language of choice not have it built-in

Possible explanations:
- *object detection* models are usually trained with real images of objects, whereas the shapes in maps are mostly silhouettes really
	- this could be solved by using (or training) a custom *object detection* model based on silhouettes

## Contents

*notebook/*
- [.NET interactive notebooks](https://github.com/dotnet/interactive) used for exploration
	- also gives an overview on how the project works
