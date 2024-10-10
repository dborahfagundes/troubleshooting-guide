# Bad Form Behaviors ❌

## The Problem:

Poor form validation, improper feedback on submission, or incorrect field types can lead to bad user experience.

## Solutions:

Implement client-side validation with proper feedback using JavaScript or HTML5 
built-in validation.

``` html
<form id="signupForm">
  <input type="email" id="email" required>
  <span class="error-message"></span>
  <button type="submit">Submit</button>
</form>

<script>
  const form = document.getElementById('signupForm');
  form.addEventListener('submit', function(e) {
    e.preventDefault();
    const emailInput = document.getElementById('email');
    if (!emailInput.validity.valid) {
      document.querySelector('.error-message').textContent = 'Please enter a valid email!';
    }
  });
</script>
```
