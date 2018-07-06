# app_layout_example

A web app that uses [AngularDart](https://webdev.dartlang.org/angular) and
[AngularDart Components](https://webdev.dartlang.org/components).

Created from templates made available by Stagehand under a BSD-style
[license](https://github.com/dart-lang/stagehand/blob/master/LICENSE).

Combines stock Stagehand app with [Angular Components app layout example](https://github.com/dart-lang/angular_components_example/tree/master/example/app_layout_example/lib)

With the `MaterialListItemComponent` enabled, I see an empty drawer pane and console output:

```
dart_sdk.js:101652 EXCEPTION: No provider found for DomService
STACKTRACE:
dart:sdk_internal                                                      throw
package:angular/src/di/injector/injector.dart 19:3                     throwsNotFound
package:angular/src/di/injector/injector.dart 90:14                    get
package:angular/src/core/linker/app_view.dart 313:28                   injectorGet
package:app_layout_example/app_component.template.dart 424:105         build
package:angular/src/core/linker/app_view.dart 230:12                   create
package:angular/src/core/linker/template_ref.dart 27:9                 createEmbeddedView
package:angular/src/core/linker/view_container.dart 93:42              createEmbeddedView
package:angular_components/content/deferred_content.dart 49:32         [_setVisible]
package:stack_trace                                                    arg
package:angular/src/core/zone/ng_zone.dart 190:16                      arg
dart:sdk_internal                                                      runUnary
package:angular/src/core/zone/ng_zone.dart 187:18                      [_runUnary]
dart:sdk_internal                                                      add
package:angular_components/app_layout/material_drawer_base.dart 56:19  ngOnInit
package:app_layout_example/app_component.template.dart 257:54          detectChangesInternal
package:angular/src/core/linker/app_view.dart 398:7                    detectChanges
package:app_layout_example/app_component.template.dart 675:16          detectChangesInternal
package:angular/src/core/linker/app_view.dart 398:7                    detectChanges
package:angular/src/core/linker/view_ref.dart 106:12                   detectChanges
package:angular/src/core/change_detection/host.dart 168:18             [_runTick]
package:angular/src/core/change_detection/host.dart 144:15             tick
package:angular/src/core/application_ref.dart 104:5                    [_loadComponent]
package:angular/src/core/application_ref.dart 97:21                    src__runtime__optimizations.unsafeCast.run.dart.fn
package:angular/src/core/change_detection/host.dart 250:18             runInZone.dart.fn
package:angular/src/core/zone/ng_zone.dart 178:16                      parent.run.dart.fn
dart:sdk_internal                                                      run
package:angular/src/core/zone/ng_zone.dart 175:18                      [_run]
dart:sdk_internal                                                      run
package:angular/src/core/zone/ng_zone.dart 327:22                      run
package:angular/src/core/application_ref.dart 138:49                   runInZone
package:angular/src/core/change_detection/host.dart 248:5              run
package:angular/src/core/application_ref.dart 67:23                    bootstrap
package:angular/src/bootstrap/run.dart 188:16                          runApp
main.dart 5:3                                                          main
main.dart.bootstrap.js 681:12                                          <fn>

dart:sdk_internal                                               listen
package:angular_components/content/deferred_content.dart 81:58  new
package:app_layout_example/app_component.template.dart 127:37   build
package:angular/src/core/linker/app_view.dart 230:12            create
package:app_layout_example/app_component.template.dart 668:16   build
package:angular/src/core/linker/app_view.dart 240:12            createHostView
package:angular/src/core/linker/component_factory.dart 112:20   create
package:angular/src/core/application_ref.dart 68:37             src__runtime__optimizations.unsafeCast.run.dart.fn
package:angular/src/core/change_detection/host.dart 250:18      runInZone.dart.fn
package:angular/src/core/zone/ng_zone.dart 178:16               parent.run.dart.fn
dart:sdk_internal                                               run
package:angular/src/core/zone/ng_zone.dart 175:18               [_run]
dart:sdk_internal                                               run
package:angular/src/core/zone/ng_zone.dart 327:22               run
package:angular/src/core/application_ref.dart 138:49            runInZone
package:angular/src/core/change_detection/host.dart 248:5       run
package:angular/src/core/application_ref.dart 67:23             bootstrap
package:angular/src/bootstrap/run.dart 188:16                   runApp
main.dart 5:3                                                   main
main.dart.bootstrap.js 681:12                                   <fn>
```

With the `MaterialListItemComponent` removed, there are no errors but the list items are not dispayed correctly.

```
$ dart --version
Dart VM version: 2.0.0-dev.67.0 (Unknown timestamp) on "linux_x64"
```

