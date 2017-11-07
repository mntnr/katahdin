# Katahdin  
  
> Better topic and keyword suggestions based on your code  
  
**This is a work in progress (WIP). Our reasoning for the final product is below.**  
  
## Mission  
  
Right now, every developer needs to manually think of keywords for their code bases, if they want them to be easily indexable, searchable, and understood by other developers. These keywords can occur in a variety of different places - for instance, in your `package.json` if you are writing JavaScript for npm, or in your GitHub repository’s topics, if you are working on GitHub, or in your GemSpec, your README, and so on. For each case, slightly different keywords make sense - it doesn’t help to tell npm that you are writing a JavaScript module, while it may be useful to set a `js` topic on GitHub.   
  
Importantly, writing these keywords takes effort, and the effort isn’t easily synced. Sure, there are packages which can automatically convert keywords in your manifests into topics on GitHub - I wrote one at [build-a-space](https://github.com/mntnr/build-a-space) - but this still requires you to do the hard work of thinking them up in the first place.   
  
What this workflow doesn’t do is: 

- Optimize topics for discovery  
- Optimize topics for each different venue where they will be seen
- Ensure that your topics are relevant to your codebase
- Automatically come up with topics for you.  
  
All of these things are — or will be — possible with Katahdin.  
  
## How this works  
  
First, we automatically get any topics we can from your manifest files or your GitHub Repository. Why wouldn’t we - the work is already done!  
  
Then, we pull topics from your high-level documentation. This means your README, GitHub description, and any other documents you may have committed in your code which are in plaintext and are useful. We extract topics using a combination of Named  Entity Recognition, noun-phrase extraction, and topic modeling. Then, we cross-check these topics against databases of keywords provided or gotten from GitHub and NPM. 

We then automatically serve a list of suspected relevant topics to you. You can do this in your CLI, or you can integrate it programmatically into your codebase using normal JavaScript imports. If you accept the topics, we’ll automatically open a PR for you to the relevant repository, and automatically try to set the topics using your GitHub API key.  
    
## Maintainers  
  
[Richard Littauer](https://github.com/RichardLitt) and [Maintainer Mountaineer](https://maintainer.io) maintain this. Interested in helping out? We’re always looking for more collaborators.

## Contribute  
  
Want to help with the details?  
  
Great. Check out the code in this repository. Are you here a bit early? That’s OK, too - this document was written _before_ the code was written, as a way of making it clear from the get-go that this was a good idea and that there’s a story to attach the effort too. Manifesto-driven-development helps us stay motivated and clear on what we’re doing.
  
[Jump into the issues](https://github.com/mntnr/katahdin/issues) if you want to help out. Ask questions! Peek around! Submit PRs!  
  
Please make sure your actions here conform to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). 
    
### Why Katahdin?  
  
Because this is a project by [Maintainer Mountaineer](https://maintainer.io). At some point, naming is difficult, so we decided to go with something arbitrary. Katahdin is the highest mountain in Maine. 

## License  
  
All work in this repository will be under the [MIT license](LICENSE) © Burnt Fen Creative LLC 2017.
  
