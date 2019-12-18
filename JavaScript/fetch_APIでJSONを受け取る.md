# fetch API で Jsonを受け取る


```js
      const formData = new FormData(formElement);
      const url = '......';
      const response = await fetch(url, {
          method: 'POST',
          body: formData
      });
      if (response.ok) {
          const person = await response.json();
          resultElement.value = 'Result: ' + person.name;
      };
```        

