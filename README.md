# TreeSelect all-mode tag removal

Browser evidence for https://github.com/Tencent/tdesign-vue-next/issues/6753.

Both screenshots use the issue's Guangdong/Guangzhou/Shenzhen data and the real Vue TreeSelect component and styles. Select Guangdong, then close the Shenzhen tag and reopen the popup.

- Before: upstream develop `21902527568003ed881cd342d5ddc63c7bf26125`; Shenzhen remains checked although its tag was removed.
- After: the fix removes the redundant Guangdong value, leaving Guangzhou selected and Guangdong indeterminate. The removal emits one change event.

Captured with Chromium 143. No external API or private user data is included.
