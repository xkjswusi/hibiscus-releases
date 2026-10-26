# hibiscus-releases

Release files for Hibiscus Korean Dictionary (槿花辭典 · 근화 사전), an offline Korean dictionary for Android made by The Coldscholar Studio.

## Language packs

The app ships with Korean definitions, English and Chinese. Japanese, Vietnamese, French and Spanish are optional language packs, and the release [`packs-1`](https://github.com/xkjswusi/hibiscus-releases/releases/tag/packs-1) holds them: one gzip-compressed SQLite file per language, 3.1–3.3 MB each, and `SHA256SUMS`.

The app downloads a pack only when its reader taps Download or Update on its Language packs screen. It checks the file's size and SHA-256 against values built into the app, refuses a file that does not match, and installs the pack in its private storage, where it works without a connection. The app does not check for updates or connect at any other time.

A published release's files are never replaced. Each version of the app names the release it reads, so a new set of packs gets a new tag (`packs-2`). The app never reads the "latest" release.

To check a download, put it beside `SHA256SUMS` and run `sha256sum -c --ignore-missing SHA256SUMS`.

## Licence and attribution

The packs hold the equivalents (translations of headwords and definitions) of the **Korean Basic Dictionary (한국어기초사전)** by the National Institute of Korean Language (국립국어원), [krdict.korean.go.kr](https://krdict.korean.go.kr), licensed under [CC BY-SA 2.0 KR](https://creativecommons.org/licenses/by-sa/2.0/kr/). Hibiscus reformatted them into one SQLite file per language. These adapted files are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International licence](LICENSE) (CC BY-SA 4.0) by The Coldscholar Studio.

The app's privacy policy, the sources of all its data and their licences are at [github.com/xkjswusi/hibiscus_dict_data](https://github.com/xkjswusi/hibiscus_dict_data), where the full dataset will be published with the app's first release.
