# dragontea
The cover id is genrated from the url field in the json. It uses the default hashing in rust. An overlap in ids is unlikly due to the small ammount of items
```rs
pub fn generate_id_from_url(url: &str) -> u64 {
    let mut hasher = DefaultHasher::new();
    url.hash(&mut hasher);
    hasher.finish()
}
```
