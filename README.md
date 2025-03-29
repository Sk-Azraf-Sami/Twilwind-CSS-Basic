# Tailwind-CSS-Basic

## Link: https://play.tailwindcss.com/z0s2Y1uol0
## HTML File: 

```html
<div class="bg-violet-200 h-10 w-full border-2 border-violet-600 rounded-md my-2 p-6 flex justify-center items-center"> 
<h1 class="text-center text-lg text-red-400 mt-2 font-mono font-extrabold text-[30px]">Hello</h1>
</div>

<!--JIT JUST IN TIME COMPILER--> 

<!--Position--> 
<div class="mt-10 flex justify-end space-x-6"> 
  <div class="h-16 w-16 rounded-full bg-blue-500"></div>
  <div class="h-16 w-16 rounded-full bg-orange-500"></div>
  <div class="h-16 w-16 rounded-full bg-green-500"></div>
</div>

<div class="mt-20 flex flex-col items-center space-y-6"> 
  <div class="h-16 w-16 rounded-full bg-blue-500"></div>
  <div class="h-16 w-16 rounded-full bg-orange-500"></div>
  <div class="h-16 w-16 rounded-full bg-green-500"></div>
</div>

<div class="mt-20 grid grid-cols-3 gap-2 mx-2"> 
  <div class="h-16 rounded-full bg-blue-500"></div>
  <div class="h-16 rounded-full bg-orange-500"></div>
  <div class="h-16 rounded-full bg-green-500"></div>
</div>

<!--responsive design--> 
<!-- larger screen style overrride style of smaller screen--> 
<!--mobile first desin--> 
<div class="sm:bg-amber-300 md:bg-amber-800 "> 
  <p class="text-white my-6 mx-6">I appear on screen wider than 768px</p>
</div>


<div class="max-sm:bg-amber-300 max-md:bg-amber-800 "> 
  <p class="text-white my-6 mx-6">I appear on screen wider than 768px</p>
</div>

<!--dark mode--> 
<div class="bg-white dark:bg-black text-black dark:text-white"> 
Dark mode disabled!
</div>

<!--custom style--> 
<div class=" mt-3 bg-[#4e1414] p-[16px] text-[20px] text-ntm">
  Test
</div>

<!--make button--> 
<div class="card"> 
  <h3>Writes about NTM</h3>
  <p>Miss so much, dreaming and fear of losing always</p> 
  <button
  id="toggleDark"
  onclick="document.body.classList.toggle('dark')"
  >Toggle Dark Mode</button>
</div>

<!--Components library shadcn--> 
<!--https://ui.shadcn.com/-->

<!--change default accent browser color-->
<div class="text-white ml-2 my-4 flex flex-col"> 
  <label><input type="checkbox" checked/> Browser Default</label>
  <label><input type="checkbox" class="accent-pink-500" checked/> Customized</label>
</div>

<!--Fluid Text--> 
<p class="text-[min(10vw,70px)]">Something Fluid</p>

<!--File--> 
<!--https://tailwindcss.com/docs/hover-focus-and-other-states#file-->
<input
  type="file"
  class="file:mr-4 file:rounded-full file:border-0 file:bg-violet-50 file:px-4 file:py-2 file:text-sm file:font-semibold file:text-violet-700 hover:file:bg-violet-100 dark:file:bg-violet-600 dark:file:text-violet-100 dark:hover:file:bg-violet-500 ..."
/>

<!--Highlight--> 
<!--https://tailwindcss.com/docs/hover-focus-and-other-states#selection-->
<div class="selection:bg-fuchsia-300 selection:text-fuchsia-900">
  <p class="my-4 mx-2">
    So I started to walk into the water. I won't lie to you boys, I was terrified. But I pressed on, and as I made my
    way past the breakers a strange calm came over me. I don't know if it was divine intervention or the kinship of all
    living things but I tell you Jerry at that moment, I <em>was</em> a marine biologist.
  </p>
</div>

<!--Less Javascript--> 
<!--Accordion--> 
<!--https://tailwindcss.com/docs/hover-focus-and-other-states#openclosed-state-->
<details class="border border-transparent open:border-black/10 open:bg-gray-100 ..." open>
  <summary class="text-sm leading-6 font-semibold text-gray-900 select-none">Why do they call it Ovaltine?</summary>
  <div class="mt-3 text-sm leading-6">
    <p class="text-black">The mug is round. The jar is round. They should call it Roundtine.</p>
  </div>
</details>


<!--caret--> 
<textarea class="caret-pink-500 ... my-5 border-4 border-black-500"></textarea>
```

## CSS file 

```css
@import "tailwindcss";

@custom-variant dark (&:where(.dark, .dark *));

@theme {
  --color-ntm: #838383;
}

body {
  background-color: rgb(28, 45, 61);
}

@layer base {
  h3 {
    @apply text-base font-medium tracking-tight text-slate-900 dark:text-white;
  }

  p {
    @apply mt-2 text-sm text-slate-500 dark:text-blue-100;
  }

  button {
    @apply mt-8 rounded-md bg-blue-100 px-4 py-2 text-sm font-medium text-blue-900;
  }
}

@layer components {
  .card {
    @apply m-10 rounded-lg bg-white px-6 py-8 shadow-xl ring-1 ring-slate-900/5 dark:bg-black;
  }
}

@utilities flex-center{
  @apply flex justify-center items-center 
} 
```

## Output 
![image](https://github.com/user-attachments/assets/374f3ff7-c042-4eaa-914a-d639c47452aa)
