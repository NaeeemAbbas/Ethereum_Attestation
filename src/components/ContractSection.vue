<script setup>
// If you had any JavaScript logic, functions, or reactive variables,
// they would go directly here. For this static layout, we don't need much.

// You would import any background images if you were bundling them via Vite/Webpack
// For simplicity, here we're still using direct paths assuming they are in 'public' or similar.
// import leftBgImage from '@/assets/your-left-background-image.png';
// import rightBgImage from '@/assets/your-right-background-image.png';

// You could also define props if this component were to receive data:
// import { defineProps } from 'vue';
// const props = defineProps({
//   headerText: String,
//   leftCode: String,
//   rightCode: String,
// });
</script>

<template>
  <div class="min-h-screen bg-gray-50 flex flex-col items-center py-12 px-4 sm:px-6 lg:px-8">
    <h1 class="text-3xl sm:text-4xl font-extrabold text-gray-900 text-center mb-12">
      Two simple contracts <br /> for any use case.
    </h1>
    <p class="text-center mb-4 pb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias, sit? Explicabo <br>consequuntur aperiam maiores praesentium non expedita, aliquam aut impedit.</p>
    <div class="relative w-full max-w-7xl flex justify-center items-center">
      <div
        class="absolute left-0 top-1/2 -translate-y-1/2 hidden lg:block bg-repeat-y bg-contain"
        :style="{ backgroundImage: 'url(\'path/to/your-left-background-image.png\')', width: '250px', height: '100%' }"
      ></div>
      <div
        class="absolute right-0 top-1/2 -translate-y-1/2 hidden lg:block bg-repeat-y bg-contain"
        :style="{ backgroundImage: 'url(\'path/to/your-right-background-image.png\')', width: '250px', height: '100%' }"
      ></div>

      <div class="bg-[#1a202c] text-white p-8 sm:p-12 rounded-lg shadow-xl max-w-4xl w-full z-10 flex flex-col lg:flex-row gap-8">
        <div class="flex-1">
          <h2 class="text-xl sm:text-2xl font-semibold mb-6">Create any scheme for your use case.</h2>
          <pre class="bg-[#2d3748] p-4 rounded-md overflow-x-auto text-sm sm:text-base">
            <code class="language-js">
              struct JournalProof &#123;
                // A unique identifier of the schema.
                bytes32 uid;
                // Optional schema resolver contract
                address resolver;
                // Whether the schema allows revocations explicitly
                bool revocable;
                // Custom specification of the schema.
                string schema;
              &#125;
            </code>
          </pre>
        </div>

        <div class="flex-1">
          <h2 class="text-xl sm:text-2xl font-semibold mb-6">Attest with any scheme.</h2>
          <pre class="bg-[#2d3748] p-4 rounded-md overflow-x-auto text-sm sm:text-base">
            <code class="language-js">
              struct Attestation &#123;
                // A unique identifier of the schema.
                bytes32 uid;
                // The UID of the related attestation.
                bytes32 refUID;
                // The time when the attestation was created.
                uint64 time;
                // The time when the attestation expires.
                uint64 expirationTime;
                // The time when the attestation was revoked.
                uint64 revocationTime;
                // The recipient of the attestation.
                address recipient;
                // The attester/sender of the attestation.
                address attester;
                // Whether the attestation is revocable.
                bool revocable;
                // Custom attestation data.
                bytes data;
              &#125;
            </code>
          </pre>
        </div>
      </div>
    </div>

    <div class="mt-12 flex flex-col sm:flex-row items-center justify-center text-gray-700 text-sm sm:text-base">
      <div class="flex items-center space-x-2 mb-4 sm:mb-0 sm:mr-6">
        <svg class="w-6 h-6 text-gray-700" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            fill-rule="evenodd"
            d="M10 0C4.477 0 0 4.477 0 10c0 4.419 2.865 8.163 6.839 9.48.5.09.682-.217.682-.483 0-.237-.008-.867-.013-1.7-2.782.604-3.369-1.34-3.369-1.34-.454-1.154-1.11-1.464-.356-1.545.83-.058 1.265.807 1.265.807.735 1.258 1.931.892 2.404.682.075-.53.288-.892.525-1.097-1.838-.208-3.77-.919-3.77-4.076 0-.899.32-1.635.85-2.217-.085-.208-.369-1.043.08-2.17 0 0 .692-.222 2.27.848.659-.183 1.37-.275 2.08-.278.71 0 1.42.095 2.079.278 1.577-1.07 2.269-.848 2.269-.848.45 1.127.162 1.962.08 2.17.53.582.85 1.318.85 2.217 0 3.165-1.936 3.865-3.784 4.07.295.253.56.756.56 1.523 0 1.097-.01 1.98-.01 2.246 0 .267.18.577.688.484C17.135 18.164 20 14.419 20 10c0-5.523-4.477-10-10-10z"
            clip-rule="evenodd"
          ></path>
        </svg>
        <span>What will you build?</span>
      </div>
      <p>Go get started with EAS <a href="#" class="text-blue-600 hover:underline"> @ethereum-attestation-service/eas-contracts -></a></p>
    </div>
  </div>
</template>

<style scoped>
/*
  With Tailwind CSS, you typically put most styling directly in the template.
  The `scoped` style block is usually reserved for:
  - Custom utility classes you define yourself (less common with Tailwind)
  - Overriding Tailwind's default behavior for specific elements (rarely needed)
  - Complex CSS that cannot be expressed purely with Tailwind utility classes
    (e.g., specific background image manipulations beyond simple utility classes,
    or more complex pseudo-elements).

  For the background images, I've used inline styles with `:style` binding
  because the exact path will depend on your project setup (public folder vs. assets folder handled by bundler).
  If you are using Vite or Webpack and importing images, you would replace the hardcoded URL string
  with the imported variable.
*/

/* Example for explicit `pre` and `code` styling for consistent font, if not handled globally */
pre {
  white-space: pre-wrap; /* Ensures text wraps within the code block */
  word-break: break-all; /* Breaks long words if they exceed the container */
}

code {
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, Courier, monospace;
}
</style>