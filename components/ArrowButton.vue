<template>
  <svg
    width="64"
    height="10"
    xmlns="http://www.w3.org/2000/svg"
  >
    <g>
      <path
        stroke="#000"
        fill="#000"
        transform="rotate(90 61.57258224487305,5.000000953674321)"
        d="m59.14517,6.65839l2.42742,-3.31678l2.42742,3.31678l-4.85483,0z"
      />
      <line
        stroke="#000"
        stroke-width="1.2"
        fill="none"
        y2="5"
        x2="61.10123"
        y1="5"
        x1="0"
      >
      </line>
    </g>
  </svg>
</template>

<script>
export default {
};
</script>

<style lang="postcss">
.anim {
  @apply relative;
}
.anim::before {
  content: "";
  @apply absolute top-0 left-0 h-28 w-28 bg-white;
  transition: width 0.3s;
}
.anim::hover::before {
  @apply w-full;
}
</style>