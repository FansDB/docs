---
title: Scraping scenes from FansDB
---

There are several ways to scrape scenes from FansDB via Stash. From automatic to manual. Each has its own advantages and disadvantages.

- [Tagger](/guides/scraping-scenes-from-fansdb/#tagger) (recommended) - partially automatic, great accuracy
- [Identify](/guides/scraping-scenes-from-fansdb/#identify) - fully automatic, mediocre accuracy
- [Scrape with...](/guides/scraping-scenes-from-fansdb/#scrape-with) - fully manual, great accuracy

## Prerequisites

### Enable perceptual hashes (pHash)

1. Go to :fontawesome-solid-gear: **Settings** > **Tasks**.
1. Under **Library** heading find configuration options for Scan task and enable **Generate perceptual hashes** option.
1. Under **Generated Content** heading find configuration options for Generate task and enable **Perceptual hashes** option.

Scan task and its options are applied when the content is being added to the database the first time.

Generate task and its options are applied when you want to generate additional things for content that is already in your database.

### Configure FansDB endpoint

1. Go to :fontawesome-solid-gear: **Settings** > **Metadata Providers**.
1. Under **Stash-box Endpoints** heading click **Add** and include the details of FansDB stash-box instance.
1. Click **Test Credentials** to make sure everything is correct.
1. Click **Confirm** to save the endpoint.

## Tagger

Recommended to people that value accuracy the most. It can automatically go through scenes and match them based on perceptual hash, but object creation and verification is left to you and nothing is saved until you click **Save**.

1. Open :fontawesome-solid-video: **Scenes** page.
1. Change the view mode to :fontawesome-solid-tags: **Tagger**.
1. Under **Source** select `stash-box: FansDB` instance.
1. Opposite the **Source** click on the :fontawesome-solid-gear: to open configuration.
    1. You can configure **Performer genders** if you want to exclude certain genders from being scraped.
    1. You can disable **Set scene cover image** if you prefer to keep your existing cover.
    1. You can enable **Set tags** if you want to be shown all the crowdsourced tags the scene has on the FansDB instance. You can also choose to either overwrite or merge with existing tags on scene.
    1. You can enable **Mark as Organized on save** which will apply :fontawesome-solid-box: organized flag.

        ??? info "Organized flag"
            All scenes marked as organized will be ignored by automatic tasks like identify and auto tag.

1. Click on **Scrape All** and look through the results. Add missing objects and click **Save**.
    1. If you got returned **No results found**, you can try using query method. You can enter title, performer, release date, or studio and click **Search**. Keep in mind that sometimes fewer details are better.
    1. If you know the scene exists on FansDB instance, but it wasn't found, you can input the exact UUID (xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx) from scene link in the *Query** field, click **Search** and it will return that exact scene.
1. For scenes that you clicked **Save** on, you will be prompted to submit your fingerprints (file hashes) back to the instance to help improve the accuracy for everyone else. Scroll to the top and click **Submit x fingerprints**.

    ??? info "Fingerprints"
        Submitted fingerprints are associated with your FansDB API key and can be managed from your account settings. No other information is sent to the FansDB instance. Privacy is paramount.

## Identify

For people that want a fully automatic option and don't mind some potential inaccuracies. The task will automatically go through all unorganized scenes and match them based on generated perceptual hash. You can also create all missing objects automatically. No manual verification is possible.

!!! warning
    Task is irreversible, so it's a good idea to [make a backup](https://docs.stashapp.cc/guides/backup-and-restore-database/){target="_blank"} before running it.

1. Go to :fontawesome-solid-gear: **Settings** and enable **Advanced mode**.
1. Go to :fontawesome-solid-gear: **Settings** > **Tasks**.
1. Under Library heading click on **Identify...**.
1. Under **Sources** select `stash-box: FansDB` instance.

    !!! info
        Identify task iterates through sources until it finds a match; once it finds a match, it will ignore all other sources for that scene.

1. Click on :fontawesome-solid-gear: next to the source to open configuration.
1. Configure **stash-box: FansDB Options**:
    1. You can configure **Performer genders** if you want to exclude certain genders from being scraped.
    1. You can disable **Set cover images** if you prefer to keep your existing cover.
    1. You can enable **Set organized flag** which will apply :fontawesome-solid-box: organized flag.
    1. You can disable **Skip matches that have more than one result** if you don't mind potentially getting more mismatched results. If enabled, it can also be tagged with a custom tag to let you know which scenes were skipped.
    1. You can disable **Skip single name performers with no disambiguation** if you don't mind potentially getting more mismatched results. If enabled, it can also be tagged with a custom tag to let you know which scenes were skipped.
1. Configure **Field Options** by clicking on :fontawesome-solid-pencil: for each field.
    1. You can confugure which strategy to use when they have existing values for that field. Valid options are:
        - **Ignore** - keep the existing value and ignore the new one.
        - **Merge** - merge the existing value with the new one.
        - **Overwrite** - overwrite the existing value with the new one.
    1. You can choose to automatically create some missing objects. They must have a strategy other than **Ignore** to be created. Available for:
        - **Studio & Parent** - enable to automatically create locally missing studios and their parent studios.
        - **Performers** - enable to automatically create locally missing performers.
        - **Tags** - enable to automatically create locally missing tags.
1. Click **Confirm** to save the source options.
1. Click **Identify** to start the task.

## Scrape with...

In addition to previous methods, there is also a completely manual way to match scenes individually.

1. Go to a scene you want to match.
1. Click on the **Edit** tab.
1. Click **Scrape with...** and select FansDB instance to match against.
1. Check the returned results, create missing objects and click **Apply**.
1. Click **Save**.

---

*Modified from [Scraping scenes via stash-box](https://docs.stashapp.cc/guides/scraping-scenes-via-stash-box/){target="_blank"} licensed under CC-BY-SA-4.0.*
