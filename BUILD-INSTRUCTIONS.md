# CiM Builder Test — инструкция по сборке

Минимальный нативный Android-проект (Kotlin) для проверки сборки debug APK через GitHub Actions.

- Приложение: CiM Builder Test
- Package ID: com.cim.buildertest
- Экран: «CiM Builder работает!»
- JDK 17, Gradle 8.9 (ставится в workflow), Android Gradle Plugin 8.5.2, Kotlin 1.9.24
- Gradle Wrapper не используется (jar-файл бинарный); Gradle устанавливает сам workflow.
- Секреты, API-ключи и платные сервисы не нужны. APK подписывается debug-ключом.

Сборка в этом проекте автором не запускалась и не проверялась.

## Как собрать
1. Убедитесь, что в репозитории в ветке main есть все файлы, включая `.github/workflows/build.yml`.
2. Push в main запускает сборку автоматически.
3. Вручную: вкладка Actions → Build debug APK → Run workflow.
4. После успеха откройте запуск и скачайте артефакт `cim-builder-test-apk` (ZIP с `app-debug.apk`).
5. Распакуйте и установите APK, разрешив установку из неизвестных источников.
