<template>
  <div class="block-bg overflow-hidden relative">
    <div class="block-title">
      <div class="w-full flex justify-between items-center">
        <span>Preview</span>
        <!-- <ToolsDropdown /> -->
      </div>
    </div>
    <div class="absolute inset-0 pt-12 p-4 h-full">
      <slot />
    </div>
    <!-- <PreviewToolbar /> -->
  </div>
</template>
