# Scenes

!!! warning
    Repeat offenders who decide to ignore comments asking for corrections will lose their EDIT privileges.

## Mandatory details

To submit a new scene, some minimum required information needs to be included. 

<div class="annotate" markdown>
- :fontawesome-solid-circle-exclamation: Title
- :fontawesome-solid-circle-exclamation: Date(1)
- :fontawesome-solid-circle-exclamation: Credited or mentioned performers
- :fontawesome-solid-circle-exclamation: Studio
- :fontawesome-solid-circle-exclamation: Perceptual hash (pHash)[^1]
</div>
1.  Required by the software. In cases where date is not known, use placeholder `1970` or `1970-01-01`. 

## Titles

<div class="annotate" markdown>
Due to networks not having a set structure, use the following order to decide which one applies to your case:

1. Official title(1)
1. User generated title
1. Title adapted from the description
1. A combination of username and date
1. Username

Limitations:

1. Do not add titles that have Unicode characters used for stylistic purpose.(2) Except for emojis.
1. Titles must be contained to a single line.(3) 
</div>
1.  In cases where the official title is not in English, a translated version needs to be added to the details section.
2.  This is to prevent various Unicode characters that use weird fonts. Different characters from various alphabets is allowed.
3.  Some sources can have titles span multiple lines. This is not shown in the `Details` tab, but the fully rendered title is visible in the `Confirm` tab. 

## Dates

1. Valid date formats are `YYYY-MM-DD`, `YYYY-MM` or `YYYY`.
1. In cases where the scene was released multiple tiles, the earliest known date should be used.
1. In cases where date is not known, use placeholder `1970` or `1970-01-01`. 
1. In cases where date is in conflict due to timezones, use UTC as a baseline. 

## Performers

<div class="annotate" markdown>
1. All credited or mentioned performers must be added.(1) 
1. Uncredited performers can be tagged with an appropriate missing performer meta tag.[^2](2)
1. Mainstream or guest performers who don't have an account on FansDB approved network should be omitted.[^3](3)
</div>
1.  Performers must meet [mandatory performer requirements](/performers/#mandatory-details). 
2.  Adding these tags are optional, but very helpful.
3.  This can often happen with professional studios that re-distribute their content on these independent creator platforms without performers having personal accounts. 

## Studios

1. The selected studio must use the account name, not the network name.
1. In cases where content is watermarked by the network, the selected studio must match the account name of that watermark. 

??? example
    - [`OnlyFans (network)`](https://fansdb.cc/studios/73e83206-90b0-41b8-acf5-3d74a244ad5a){target=_blank} is a network.  
    - [`_boyo_19 (OnlyFans)`](https://fansdb.cc/studios/e60a6efa-6f9f-4b01-a530-b5d09d8538dc){target=_blank} is a studio.

## Details

<div class="annotate" markdown>
1. In cases where scene description is not in English, add a translated version below it.
1. Do not add details that have Unicode characters used for stylistic purpose.(1) Except for emojis.
</div>
1.  This is to prevent various Unicode characters that use weird fonts. Different characters from various alphabets is allowed.

## Links

<div class="annotate" markdown>
1. Only links that have a matching site can be added.
1. Defunct links can be added and must be kept.(1)
1. Studio links that are different from the selected studio and doesn't match the watermark can be included.
</div>
1.  Defunct links are kept for prosperity and ability to lookup information from archives.

!!! tip
    When adding links, make sure to click `Add` when adding links manually. 

??? "Suggest a site"
    If there is a site you would like to be added, you can suggest them [in this document](https://cryptpad.fr/sheet/#/2/sheet/edit/6DWaSIONfZN4Ty0S2+nEpT6q/){target=_blank} and we will review it.


## Cover images

<div class="annotate" markdown>
Due to networks not having a set structure, use the following order to decide which one applies to your case:

1. Studio provided cover
1. User generated cover
1. Scene thumbnail
1. No cover

Limitations:

1. Do not add animated, drawn, 2D or 3D covers.
1. Do not cover images that have watermarks from pirate sites.(1)
</div>
1.  Blurred, cropped or otherwise hidden watermarks are acceptable.

## Content distribution

1. In cases where scenes are distributed on multiple networks or, different accounts must have separate entries for each of them.
1. In cases where scenes from approved networks are later distributed on unapproved platforms are permissible.  

## Duplicates

1. Scenes that are identical and released on the same account and same approved network should be merged into one and submitted with the earliest known metadata.
1. Scenes that are identical and released on a different account, but on the same approved network, should have separate entries.
1. Scenes that are identical but released on different account and different approved network should have separate entries.

## Trailers

1. Promotional trailers that are posted on the studio are allowed, but should be tagged with an appropriate meta tag.[^4]

[^1]: Perceptual hash (pHash) can be generated in [Stash](https://github.com/stashapp/stash){target=_blank} by enabling `Generate perceptual hashes` option in Settings > Tasks. 
[^2]: These tags are: [`Missing Performer (Female)`](https://fansdb.cc/tags/0da5f9d7-a766-4eef-887c-fece963feec2){target=_blank}, [`Missing Performer (Male)`](https://fansdb.cc/tags/3ce1c8e4-fbdf-460c-87cd-749a8cf40e83){target=_blank}, [`Missing Performer (Trans)`](https://fansdb.cc/tags/e2b45727-e740-4ff2-b112-a6657727f4bf){target=_blank}.
[^3]: These scenes can be optionally tagged with [`Unverified Performer`](https://fansdb.cc/tags/daa452de-e324-4b0c-811a-4c2e0a277535){target=_blank} tag and mention the performer's name in the scene details. 
[^4]: Tag: [`Trailer`](https://fansdb.cc/tags/d1afaa79-0b33-4bb1-91d0-3d2b3c4f735b){target=_blank}.