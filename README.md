# Como burlar a verificação de idade no Archive do website
```bash
document.querySelectorAll(
  '.age-gate, .age-gate-overlay, .age-gate-wrapper'
).forEach(el => el.remove());

document.documentElement.classList.remove('age-gate-restricted');
document.body.classList.remove('age-restriction');

document.querySelectorAll('body > *').forEach(el => {
  if (el.matches('header, main, footer, #page, .site-content, .site-header, .site-footer')) {
    el.style.display = '';
    el.style.visibility = 'visible';
    el.style.opacity = '1';
  }
});
```
