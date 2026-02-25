# Deploying CX to a Non-Default Virtual Instance
You can specify the virtual instance in three different ways.

## ✅ Option 1 — Using `gradle.properties`

- Open `gradle.properties`
- Add the following line:

```properties
liferay.virtual.instance.id=my.web.id
```

- Run the deploy command:

```bash
./gradlew deploy
```

---

## ✅ Option 2 — Using `settings.gradle`

- Open `settings.gradle`
- Add:

```groovy
gradle.liferayWorkspace {
    virtualInstanceId = "my.web.id"
}
```

- Deploy:

```bash
./gradlew deploy
```

---

## ✅ Option 3 — Command Line (Recommended)

- Run deploy with a property override:

```bash
./gradlew deploy -Pliferay.virtual.instance.id=my.web.id
```
