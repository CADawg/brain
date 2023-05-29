```go
queries := strings.Split(string(sql), ";")  
  
for _, query := range queries {  
   // skip empty queries (it throws an error otherwise)  
   if strings.TrimSpace(query) == "" {  
      continue  
   }  
  
   _, err = db.NewQuery(query).Execute()  
  
   if err != nil {  
      return err  
   }  
}
```

#Go #SQL #MariaDB #MySQL