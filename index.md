---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<div class="flex flex-col gap-2 max-w-xl w-full">
  <div class="flex gap-2 items-center">
    <a
      class="font-sans px-2 py-1 text-sm bg-gray-100 rounded-xl flex items-center gap-2 interact-bounce text-gray-700"
      href="/"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        aria-hidden="true"
        data-slot="icon"
        class="h-4 w-4"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M10.5 19.5 3 12m0 0 7.5-7.5M3 12h18"
        ></path></svg
      >Go back</a
    ><svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      stroke-width="1.5"
      stroke="currentColor"
      aria-hidden="true"
      data-slot="icon"
      class="h-3 w-3 text-gray-400"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="m8.25 4.5 7.5 7.5-7.5 7.5"
      ></path></svg
    ><span class="text-sm border text-gray-500 rounded-xl px-2 py-1"
      >The blog</span
    >
  </div>
  <article class="py-4 sm:pb-24 markdown">
    <div class="flex flex-row items-center justify-end mb-4 gap-2">
    <div class="text-xl font-serif">{{page.title}}</div>
    <a
      href="https://github.com/sfcompute/tinynarrations"
      class="font-sans px-2 py-1 text-sm bg-blue-50 rounded-lg flex items-center gap-2 interact-bounce w-max h-max no-underline"
      style="text-decoration-line: none"
      ><span class="line-through">Twitter</span>𝕏
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        aria-hidden="true"
        data-slot="icon"
        class="h-3 w-3"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="m4.5 19.5 15-15m0 0H8.25m11.25 0v11.25"
        ></path></svg
    ></a>
<a
      href="/what-is-indie-hacking-anyway"
      class="font-sans px-2 py-1 text-sm bg-blue-50 rounded-lg flex items-center gap-2 interact-bounce w-max h-max no-underline"
      style="text-decoration-line: none"
      >What is indie hacking anyway?
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        aria-hidden="true"
        data-slot="icon"
        class="h-3 w-3"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="m4.5 19.5 15-15m0 0H8.25m11.25 0v11.25"
        ></path></svg
    ></a>
  </div>
    <p>I'm Alireza Bashiri. I run a solo dev agency, <a class="text-black" href="x.com/al3rez">Devmason</a>, and I'm about to quit and become a full-time indie hacker soon. I often write on <a class="text-black" href="x.com/al3rez">Twitter</a>, and here I share what I learn in between.    </p>
    <h2>Posts</h2>
    <ul>
      {% for post in site.posts %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  </article>
</div>
