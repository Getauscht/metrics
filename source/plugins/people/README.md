### đ§âđ¤âđ§ People plugin

The *people* plugin can display people you're following or sponsoring, and also users who're following or sponsoring you.
In repository mode, it's possible to display sponsors, stargazers, watchers.

<table>
  <td align="center">
    <details open><summary>Related to an user</summary>
      <img src="https://github.com/lowlighter/lowlighter/blob/master/metrics.plugin.people.followers.svg">
    </details>
    <details><summary>Related to a repository</summary>
      <img src="https://github.com/lowlighter/lowlighter/blob/master/metrics.plugin.people.repository.svg">
    </details>
    <img width="900" height="1" alt="">
  </td>
</table>

The following types are supported:

| Type            | Alias                                | User metrics       | Repository metrics |
| --------------- | ------------------------------------ | :----------------: | :----------------: |
| `followers`     |                                      | âī¸                 | â                |
| `following`     | `followed`                           | âī¸                 | â                |
| `sponsoring`    | `sponsored`, `sponsorshipsAsSponsor` | âī¸                 | â                |
| `sponsors`      | `sponsorshipsAsMaintainer`           | âī¸                 | âī¸                |
| `contributors`  |                                      | â                 | âī¸                |
| `stargazers`    |                                      | â                 | âī¸                |
| `watchers`      |                                      | â                 | âī¸                |
| `thanks`        |                                      | âī¸                 | âī¸                |
| `members`       |                                      | âī¸ (organization)  | â                |


Sections will be ordered the same as specified in `plugin_people_types`.
`sponsors` for repositories will output the same as the owner's sponsors.

#### âšī¸ Examples workflows

[âĄī¸ Available options for this plugin](metadata.yml)

```yaml
- uses: lowlighter/metrics@latest
  with:
    # ... other options
    plugin_people: yes
    plugin_people_types: followers, thanks     # Display followers and "thanks" sections
    plugin_people_limit: 28                    # Limit to 28 entries per section
    plugin_people_size: 28                     # Size in pixels of displayed avatars
    plugin_people_identicons: no               # Use avatars (do not use identicons)
    plugin_people_thanks: lowlighter, octocat  # Users that will be displayed in "thanks" section
    plugin_people_sponsors_custom: octocat     # Users that will be displayed additionally in "sponsors" section
    plugin_people_shuffle: yes                 # Shuffle for varied output
```
