# Unity -> Reactive Property Converter
ReactivePropertyConverter for [ReactiveProperty](https://github.com/RimuruDev/Unity-ReactiveProperty-Helper)

Dependency: 
```json 
{
  "dependencies": {
    "com.unity.nuget.newtonsoft-json": "3.2.1",
 }
}
```

# Example

```cs
    [Serializable]
    public class HalloweenUserProgress
    {
        [JsonProperty("Currency")] 
        [JsonConverter(typeof(ReactivePropertyConverter))]
        public ReactiveProperty<int> Currency = new();

        [JsonProperty("LevelProgress")] 
        [JsonConverter(typeof(ReactivePropertyConverter))]
        public ReactiveProperty<List<LevelProgress>> LevelProgress = new();
    }
```

## Before use `[JsonConverter(typeof(ReactivePropertyConverter))]`

<img width="306" alt="image" src="https://github.com/user-attachments/assets/08a23669-4f23-412f-b5f1-4b2235c91314">

## After use `[JsonConverter(typeof(ReactivePropertyConverter))]`

<img width="230" alt="image" src="https://github.com/user-attachments/assets/321edaee-8b5a-4012-b9e0-cec0ff098ab0">
