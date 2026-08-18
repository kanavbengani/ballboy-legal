---
title: Delete Your Account
---

# Delete Your Ballboy Account

**Last updated:** August 18, 2026

> **The quickest way is in the app.** Open Ballboy, go to the **Profile** tab,
> scroll to the bottom, and tap **Delete Account**. It happens immediately and
> you don't need this page at all.

If you no longer have the app installed, sign in below with the same account
you use in Ballboy and delete it from here. Deletion is immediate and
permanent — there is no undo and no grace period.

{% raw %}
<div id="ba-widget" class="ba-card">

  <div id="ba-signin">
    <h3 class="ba-h">Sign in to your Ballboy account</h3>

    <button type="button" id="ba-google" class="ba-btn ba-btn-google">
      <svg width="16" height="16" viewBox="0 0 48 48" aria-hidden="true" focusable="false"><path fill="#FFC107" d="M43.611 20.083H42V20H24v8h11.303c-1.649 4.657-6.08 8-11.303 8-6.627 0-12-5.373-12-12s5.373-12 12-12c3.059 0 5.842 1.154 7.961 3.039l5.657-5.657C34.046 6.053 29.268 4 24 4 12.955 4 4 12.955 4 24s8.955 20 20 20 20-8.955 20-20c0-1.341-.138-2.65-.389-3.917z"/><path fill="#FF3D00" d="M6.306 14.691l6.571 4.819C14.655 15.108 18.961 12 24 12c3.059 0 5.842 1.154 7.961 3.039l5.657-5.657C34.046 6.053 29.268 4 24 4 16.318 4 9.656 8.337 6.306 14.691z"/><path fill="#4CAF50" d="M24 44c5.166 0 9.86-1.977 13.409-5.192l-6.19-5.238C29.211 35.091 26.715 36 24 36c-5.202 0-9.619-3.317-11.283-7.946l-6.522 5.025C9.505 39.556 16.227 44 24 44z"/><path fill="#1976D2" d="M43.611 20.083H42V20H24v8h11.303c-.792 2.237-2.231 4.166-4.087 5.571.001-.001.002-.001.003-.002l6.19 5.238C36.971 39.205 44 34 44 24c0-1.341-.138-2.65-.389-3.917z"/></svg>
      <span>Continue with Google</span>
    </button>

    <div class="ba-or"><span></span>or with email<span></span></div>

    <form id="ba-form" novalidate>
      <label class="ba-label" for="ba-email">Email</label>
      <input class="ba-input" id="ba-email" type="email" autocomplete="email" required>
      <label class="ba-label" for="ba-password">Password</label>
      <input class="ba-input" id="ba-password" type="password" autocomplete="current-password" required>
      <button type="submit" id="ba-submit" class="ba-btn ba-btn-primary">Sign in</button>
    </form>
  </div>

  <div id="ba-account" hidden>
    <h3 class="ba-h">Signed in as <span id="ba-who"></span></h3>
    <p class="ba-note">
      Deleting removes your profile, teams, trades, picks, chat messages, and
      push tokens, and signs you out everywhere. Leagues you created are
      deleted for everyone in them.
    </p>
    <label class="ba-check">
      <input type="checkbox" id="ba-understand">
      <span>I understand this is permanent and cannot be undone.</span>
    </label>
    <button type="button" id="ba-delete" class="ba-btn ba-btn-danger" disabled>
      Delete my account
    </button>
    <button type="button" id="ba-signout" class="ba-linkbtn">Sign out instead</button>
  </div>

  <div id="ba-done" hidden>
    <h3 class="ba-h">Your account has been deleted</h3>
    <p class="ba-note">
      Your Ballboy account and its data are gone, and your login no longer
      works. Nothing further is needed from you.
    </p>
  </div>

  <p id="ba-status" class="ba-status" role="status" aria-live="polite"></p>
</div>

<style>
  .ba-card { border: 1px solid #dfe2e5; border-radius: 8px; padding: 20px; margin: 24px 0; background: #fff; }
  .ba-h { margin: 0 0 14px; font-size: 17px; }
  .ba-label { display: block; font-size: 13px; color: #555; margin: 10px 0 4px; }
  .ba-input { width: 100%; box-sizing: border-box; padding: 9px 10px; font-size: 15px; border: 1px solid #ccd0d4; border-radius: 6px; }
  .ba-btn { display: flex; align-items: center; justify-content: center; gap: 8px; width: 100%; box-sizing: border-box; margin-top: 14px; padding: 10px 14px; font-size: 15px; font-weight: 600; border-radius: 6px; border: 1px solid transparent; cursor: pointer; }
  .ba-btn[disabled] { opacity: .5; cursor: not-allowed; }
  .ba-btn-google { background: #fff; color: #24292e; border-color: #ccd0d4; }
  .ba-btn-primary { background: #159957; color: #fff; }
  .ba-btn-danger { background: #c9302c; color: #fff; }
  .ba-linkbtn { display: block; width: 100%; margin-top: 10px; padding: 6px; background: none; border: 0; color: #666; font-size: 13px; text-decoration: underline; cursor: pointer; }
  .ba-or { display: flex; align-items: center; gap: 10px; margin: 18px 0 4px; font-size: 11px; letter-spacing: .06em; text-transform: uppercase; color: #888; }
  .ba-or span { flex: 1; height: 1px; background: #e1e4e8; }
  .ba-note { font-size: 14px; color: #444; margin: 0 0 12px; }
  .ba-check { display: flex; gap: 8px; align-items: flex-start; font-size: 14px; color: #444; }
  .ba-status { margin: 14px 0 0; font-size: 14px; min-height: 1em; }
  .ba-status.ba-err { color: #c9302c; }
</style>

<script>
(function () {
  var SUPABASE_URL = 'https://sbosoekuupsvvuywcjvn.supabase.co';
  var SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InNib3NvZWt1dXBzdnZ1eXdjanZuIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzM1ODQxMDEsImV4cCI6MjA4OTE2MDEwMX0.MoM7zwyJqLIaxu9dJ8DHkIahkdroHAtB_QS-VlRatyo';
  var API_BASE = 'https://tennis-fantasy.onrender.com';

  var el = function (id) { return document.getElementById(id); };
  var token = null;

  function status(msg, isError) {
    var s = el('ba-status');
    s.textContent = msg || '';
    s.className = 'ba-status' + (isError ? ' ba-err' : '');
  }

  function panel(name) {
    ['ba-signin', 'ba-account', 'ba-done'].forEach(function (id) {
      el(id).hidden = (id !== name);
    });
  }

  // Google comes back via the implicit flow: tokens land in the URL fragment.
  function readHash() {
    if (!window.location.hash) return;
    var p = new URLSearchParams(window.location.hash.slice(1));
    history.replaceState(null, '', window.location.pathname + window.location.search);
    if (p.get('error_description')) {
      status(p.get('error_description'), true);
      return;
    }
    if (p.get('access_token')) signedIn(p.get('access_token'));
  }

  function signedIn(accessToken) {
    token = accessToken;
    panel('ba-account');
    status('');
    fetch(SUPABASE_URL + '/auth/v1/user', {
      headers: { apikey: SUPABASE_ANON_KEY, Authorization: 'Bearer ' + token }
    })
      .then(function (r) { return r.json(); })
      .then(function (u) { el('ba-who').textContent = u.email || 'your account'; })
      .catch(function () { el('ba-who').textContent = 'your account'; });
  }

  el('ba-google').addEventListener('click', function () {
    var here = window.location.origin + window.location.pathname;
    window.location.href = SUPABASE_URL + '/auth/v1/authorize?provider=google&redirect_to=' +
      encodeURIComponent(here);
  });

  el('ba-form').addEventListener('submit', function (e) {
    e.preventDefault();
    var email = el('ba-email').value.trim();
    var password = el('ba-password').value;
    if (!email || !password) { status('Enter your email and password.', true); return; }
    el('ba-submit').disabled = true;
    status('Signing in…');
    fetch(SUPABASE_URL + '/auth/v1/token?grant_type=password', {
      method: 'POST',
      headers: { apikey: SUPABASE_ANON_KEY, 'Content-Type': 'application/json' },
      body: JSON.stringify({ email: email, password: password })
    })
      .then(function (r) { return r.json().then(function (d) { return { ok: r.ok, d: d }; }); })
      .then(function (res) {
        el('ba-submit').disabled = false;
        if (!res.ok || !res.d.access_token) {
          status(res.d.msg || res.d.error_description || 'We could not sign you in with those details.', true);
          return;
        }
        signedIn(res.d.access_token);
      })
      .catch(function () {
        el('ba-submit').disabled = false;
        status('Could not reach the sign-in service. Please try again.', true);
      });
  });

  el('ba-understand').addEventListener('change', function () {
    el('ba-delete').disabled = !this.checked;
  });

  el('ba-signout').addEventListener('click', function () {
    token = null;
    el('ba-understand').checked = false;
    el('ba-delete').disabled = true;
    panel('ba-signin');
    status('');
  });

  el('ba-delete').addEventListener('click', function () {
    if (!token) { status('Please sign in again.', true); panel('ba-signin'); return; }
    if (!window.confirm('Permanently delete your Ballboy account? This cannot be undone.')) return;
    el('ba-delete').disabled = true;
    status('Deleting your account… this can take up to a minute if our server is asleep.');
    fetch(API_BASE + '/tf_app/users/me/delete/', {
      method: 'DELETE',
      headers: { Authorization: 'Bearer ' + token }
    })
      .then(function (r) { return r.json().then(function (d) { return { ok: r.ok, d: d }; }); })
      .then(function (res) {
        if (res.ok && res.d.success) {
          token = null;
          panel('ba-done');
          status('');
          return;
        }
        el('ba-delete').disabled = false;
        status((res.d.error || res.d.detail || 'Deletion failed.') + ' Please email us using the address at the bottom of this page.', true);
      })
      .catch(function () {
        el('ba-delete').disabled = false;
        status('Could not reach our server. Please try again, or email us using the address at the bottom of this page.', true);
      });
  });

  readHash();
})();
</script>
{% endraw %}

## What gets deleted

Deleting your account permanently removes:

- your account and login credentials (you will not be able to sign back in);
- your profile — name, username, country, and avatar image;
- your leagues, teams, draft picks, trades, and daily picks;
- your chat messages and any reports you filed;
- your push notification tokens and notification settings.

## What we keep

- **Anonymized submissions.** If you sent in app feedback, we keep the text
  with your identity removed so we can still act on it.
- **Server logs.** Routine request logs (timestamps, endpoints, error states)
  age out on their normal retention schedule and are not tied to your profile
  once the account is gone.
- **Anything the law requires us to retain**, for as long as it requires.

## What this means for your leagues

Leagues you **joined** carry on for everyone else — your team and your history
in them are removed, but the league itself is untouched.

Leagues you **created** are deleted along with your account, for every member
of them: their teams, the draft, and the chat history go too. If you created a
league that other people are still playing in, email us before you delete and
we will sort the league out first.

---

If none of the above works — you signed in with Apple, you've forgotten your
password, or the form gives you an error — email **runballboy@gmail.com** with
**[Delete Account]** in the subject line, from the address on the account, and
we will delete it for you within 30 days.

See also our [Privacy Policy](./privacy) and [Terms of Service](./terms).
