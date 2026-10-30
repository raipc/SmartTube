# Карта исходников и методика

Ссылки закреплены на исследованных commit SHA. Все указанные файлы присутствовали в локальном checkout; для основных выводов прочитаны реализации и Gradle-конфигурация. Это выборочный архитектурный анализ, не аудит каждой строки.

| ID | Назначение | Исходники |
| --- | --- | --- |
| S01 | Сборка приложения | [settings.gradle](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/settings.gradle); [build.gradle](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/build.gradle); [build.gradle](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/smarttubetv/build.gradle) |
| S02 | Медиапровайдер | [core_settings.gradle](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/core_settings.gradle); [build.gradle](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/mediaserviceinterfaces/build.gradle); [build.gradle](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/build.gradle) |
| S03 | Shared-модули | [core_settings.gradle](https://github.com/yuliskov/SharedModules/blob/799cfae8a2f5c609b99e87fc673fc62de1c0199a/core_settings.gradle); [.gitmodules](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/.gitmodules) |
| S04 | Запуск | [MainApplication.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/smarttubetv/src/main/java/com/liskovsoft/smartyoutubetv2/tv/ui/main/MainApplication.java) |
| S05 | Навигация | [ViewManager.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/views/ViewManager.java); [PlaybackView.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/views/PlaybackView.java) |
| S06 | Android-зависимости presenters | [BasePresenter.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/presenters/base/BasePresenter.java) |
| S07 | Поиск | [SearchPresenter.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/presenters/SearchPresenter.java) |
| S08 | Каталог | [YouTubeContentService.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/service/YouTubeContentService.java) |
| S09 | Координация загрузки | [MediaServiceManager.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/misc/MediaServiceManager.java) |
| S10 | Провайдер | [ServiceManager.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/mediaserviceinterfaces/src/main/java/com/liskovsoft/mediaserviceinterfaces/ServiceManager.java); [YouTubeServiceManager.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/service/YouTubeServiceManager.java) |
| S11 | Player events | [PlaybackPresenter.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/presenters/PlaybackPresenter.java) |
| S12 | Выбор транспорта | [VideoLoaderController.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/playback/controllers/VideoLoaderController.java) |
| S13 | Контракт плеера | [PlayerManager.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/playback/manager/PlayerManager.java); [PlayerEngine.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/playback/manager/PlayerEngine.java) |
| S14 | ExoPlayer | [ExoPlayerController.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/exoplayer/controller/ExoPlayerController.java); [ExoMediaSourceFactory.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/exoplayer/ExoMediaSourceFactory.java) |
| S15 | Клиенты и fallback | [FormatInfoWrapper.kt](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/service/internal/FormatInfoWrapper.kt) |
| S16 | Описание источников | [MediaItemFormatInfo.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/mediaserviceinterfaces/src/main/java/com/liskovsoft/mediaserviceinterfaces/data/MediaItemFormatInfo.java) |
| S17 | Token runtime | [WebPoTokenProvider.kt](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/app/potokennp2/WebPoTokenProvider.kt); [PoTokenWebView.kt](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/app/potokennp2/generators/PoTokenWebView.kt) |
| S18 | SABR и UMP | [SabrMediaSource.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/exoplayer-amzn-2.10.6/library/sabr/src/main/java/com/google/android/exoplayer2/source/sabr/SabrMediaSource.java); [UMPDecoder.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/exoplayer-amzn-2.10.6/library/sabr/src/main/java/com/google/android/exoplayer2/source/sabr/parser/ump/UMPDecoder.java); [video_playback_abr_request.proto](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/exoplayer-amzn-2.10.6/library/sabr/src/main/proto/sabr/videostreaming/video_playback_abr_request.proto) |
| S19 | Модели и очередь | [Video.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/data/Video.java); [VideoGroup.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/data/VideoGroup.java); [Playlist.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/data/Playlist.java) |
| S20 | Состояние просмотра | [VideoStateService.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/playback/service/VideoStateService.java) |
| S21 | Preferences | [AppPrefs.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/prefs/AppPrefs.java) |
| S22 | Auth и сеть | [YouTubeSignInService.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/service/YouTubeSignInService.java); [RetrofitOkHttpHelper.kt](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/googlecommon/common/helpers/RetrofitOkHttpHelper.kt) |
| S23 | Асинхронность | [RxHelper.java](https://github.com/yuliskov/SharedModules/blob/799cfae8a2f5c609b99e87fc673fc62de1c0199a/sharedutils/src/main/java/com/liskovsoft/sharedutils/rx/RxHelper.java) |
| S24 | SponsorBlock и DeArrow | [SponsorBlockController.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/common/src/main/java/com/liskovsoft/smartyoutubetv2/common/app/models/playback/controllers/SponsorBlockController.java); [SponsorBlockService.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/block/SponsorBlockService.java); [DeArrowService.kt](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/main/java/com/liskovsoft/youtubeapi/dearrow/DeArrowService.kt) |
| S25 | Существующие тесты | [DefaultSabrChunkSourceTest.java](https://github.com/yuliskov/SmartTube/blob/4b3f333e540a1403429d1a9d86dec758e59288f9/exoplayer-amzn-2.10.6/library/sabr/src/test/java/com/google/android/exoplayer2/source/sabr/DefaultSabrChunkSourceTest.java); [YouTubeServiceManagerTest.java](https://github.com/yuliskov/MediaServiceCore/blob/40fec843eb24bc264e9c8b429fcee25068e230e2/youtubeapi/src/test/java/com/liskovsoft/youtubeapi/service/YouTubeServiceManagerTest.java) |

## Web-платформа

Проверено 30 октября 2026. Эти документы описывают платформу, но не подтверждают работоспособность конкретных YouTube endpoint из стороннего origin.

| ID | Источник | Использование |
| --- | --- | --- |
| W01 | [WHATWG Fetch](https://fetch.spec.whatwg.org/) | CORS, forbidden request headers, opaque responses |
| W02 | [W3C MSE](https://w3c.github.io/media-source/) | SourceBuffer и byte streams; развивающийся draft, не гарантия поддержки всех новых функций |
| W03 | [MDN: isTypeSupported](https://developer.mozilla.org/en-US/docs/Web/API/MediaSource/isTypeSupported_static) | MIME/codec |
| W04 | [MDN: Media Capabilities](https://developer.mozilla.org/en-US/docs/Web/API/Media_Capabilities_API/Using_the_Media_Capabilities_API) | Возможности декодирования |
| W05 | [MDN: Autoplay](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Autoplay) | Ограничения автоматического запуска |

## Воспроизведение анализа

```bash
git clone https://github.com/raipc/SmartTube.git
cd SmartTube
git checkout 4b3f333e540a1403429d1a9d86dec758e59288f9
git submodule update --init --recursive
git submodule status
```

Сначала изучить S01–S03, затем пройти поиск S07–S10 и воспроизведение S11–S18. Для повторения import census выполнить из корня:

```python
from pathlib import Path
import re
modules = ["smarttubetv", "common", "MediaServiceCore/mediaserviceinterfaces",
           "MediaServiceCore/youtubeapi", "SharedModules/sharedutils",
           "exoplayer-amzn-2.10.6/library/sabr"]
for module in modules:
    files = [p for p in Path(module).glob("src/main/**/*")
             if p.suffix in (".java", ".kt")]
    imports = sum(bool(re.search(r"^import (?:android\.|androidx\.)",
                               p.read_text(errors="replace"), re.M))
                  for p in files)
    print(module, len(files), imports)
```

Проверки документации: наличие ссылочных исходников, закреплённые SHA подмодулей, локальные Markdown-ссылки, import census и git diff --check. Runtime-тесты, Gradle-сборка и браузерное воспроизведение не выполнялись.
