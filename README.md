# VoynaSlov
This repository contains the data described in [VoynaSlov: A Data Set of Russian Social Media Activity during
the 2022 Ukraine-Russia War](https://arxiv.org/abs/2205.12382). Details on the data collection process and data statistics can be found in the paper.
Please cite the paper if you use this data set. 

```
@misc{park-etal-2022-voynaslov,
  doi = {10.48550/ARXIV.2205.12382},
  url = {https://arxiv.org/abs/2205.12382},
  author = {Park, Chan Young and Mendelsohn, Julia and Field, Anjalie and Tsvetkov, Yulia},  
  title = {VoynaSlov: A Data Set of Russian Social Media Activity during the 2022 Ukraine-Russia War},
  publisher = {arXiv},
  year = {2022},
  copyright = {Creative Commons Attribution Non Commercial Share Alike 4.0 International}
}
```

Also, if you decide to use our data, we recommend you to read the *Ethical Consideration* section in our paper, where we describe the potential biases and limitations of our data. 
** **Note that the data collection is still ongoing, and this repository is regularly updated as we collect more data.**

## Overview
VoynaSlove contains 21M+ Russian-language social media activities (i.e. tweets, posts, comments) made by Russian media outlets and by the general public during the war between Ukraine and Russia. 
The data was collected from two major platforms that are widely used in Russia: [Twitter](https://twitter.com) and [VKontakte (VK)](https://vk.com), a Russian social media platform based in Saint Petersburg commonly referred to as “Russian Facebook”. 
The main differences that distinguish our data from previously released data related to the ongoing war are its focus on Russian *media* and consideration of state-affiliation as well as the inclusion of data from *VK*, which is more suitable than Twitter for understanding Russian public sentiment considering its wide use within Russia.  

## Data Set Structure
- **media-accounts**: contains lists of account handles of Russian media accounts on Twitter and VK. 
- **search-terms**: lists search terms we used to scrape tweets from Twitter (`all.txt`). The directory also includes several subsets of terms associated with stances toward Russia, Ukraine, and the war.
- **VK**: stores ids of VK posts made by Russian media accounts (`media-posts`). It also includes the ids of users' comments left on those posts (`public-reaction`). They are grouped by 1) state-affiliation of the media (independent/state-affiliated), 2) media outlets (e.g. bbc, tvrain), and 3) date (e.g. 2022-02-24.txt).
- **Twitter**: stores the ids of Tweets made by Russian media accounts on Twitter (`media-posts`) which are structured in the same way as VK. However, `public-reaction` is different as they are tweets from API search and not associated with any Russian media. They thus are grouped by date only.

We note that the `VK` and `Twitter` directories are regularly updated as we collect more data throughout the war. Also, our data release only contains *ids* of posts and comments instead of raw texts, which can be used to recollect the actual data using [Twitter API](https://developer.twitter.com/en/docs/twitter-api) and [VK Open API](https://vk.com/dev/openapi).

## Contact
The main maintainer of this repository is @chan0park. Please feel free to reach out for further information about the data set.