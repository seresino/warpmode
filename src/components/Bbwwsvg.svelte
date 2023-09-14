<svg width="200" height="200" viewBox="0 0 312 311" fill="none" xmlns="http://www.w3.org/2000/svg">
  <g class="bbwm">
    <g class="trigger">
      <circle id="Ellipse 1" cx="156" cy="155" r="152" fill="black"/>
      <g id="arrows_rotate">
        <path id="Arrow" d="M311.77 179.322L310.03 167.132C310.01 166.982 309.81 166.952 309.75 167.092L304.42 178.482C304.36 178.602 304.5 178.732 304.62 178.662L308.58 176.422L311.5 179.462C311.61 179.572 311.8 179.482 311.78 179.322H311.77Z" fill="white"/>
        <path id="Vector" d="M308.8 174.531C299.19 246.551 239.89 302.861 166.5 307.841" stroke="white" stroke-width="2.03" stroke-miterlimit="10"/>
      </g>
      <g id="arrows_rotate-2">
        <path id="Arrow-2" d="M181.21 0.00146155L169.01 1.71147C168.86 1.73147 168.83 1.93147 168.97 1.99147L180.34 7.35147C180.46 7.41147 180.59 7.27147 180.52 7.16147L178.29 3.19146L181.34 0.28146C181.45 0.17146 181.36 -0.0185385 181.2 0.00146155H181.21Z" fill="white"/>
        <path id="Vector_2" d="M176.42 2.96143C248.42 12.7414 304.59 72.1814 309.39 145.581" stroke="white" stroke-width="2.03" stroke-miterlimit="10"/>
      </g>
      <g id="arrows_rotate-3">
        <path id="Arrow-3" d="M0.639874 135.051L2.71988 147.191C2.74988 147.341 2.94987 147.361 2.99987 147.221L8.00987 135.691C8.05987 135.571 7.92987 135.451 7.80987 135.521L3.90988 137.871L0.909878 134.911C0.799878 134.801 0.60988 134.901 0.62988 135.051H0.639874Z" fill="white"/>
        <path id="Vector_3" d="M3.75 139.751C11.33 67.4815 69.03 9.53146 142.25 2.49146" stroke="white" stroke-width="2.03" stroke-miterlimit="10"/>
      </g>
      <g id="arrows_rotate-4">
        <path id="Arrow-4" d="M136.4 310.442L148.54 308.342C148.69 308.312 148.71 308.112 148.57 308.062L137.03 303.072C136.91 303.022 136.79 303.152 136.86 303.272L139.21 307.162L136.25 310.172C136.14 310.282 136.24 310.472 136.39 310.452L136.4 310.442Z" fill="white"/>
        <path id="Vector_4" d="M141.1 307.331C68.83 299.831 10.81 242.191 3.69995 168.981" stroke="white" stroke-width="2.03" stroke-miterlimit="10"/>
      </g>
    </g>
    <g class="text">
      <text id="BLACK BEYOND" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="31" letter-spacing="0em"><tspan x="34.2598" y="168.056">BLACK BEYOND</tspan></text>
      <text id="WARP MODE" transform="matrix(0 -1 1 0 137.53 276)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="30" letter-spacing="0em"><tspan x="0" y="26.28">WARP       MODE</tspan></text>
    </g>
  </g>
</svg>

<style>
  svg {
    width: 100%;
    cursor: pointer;
    user-select: none;
  }

  /* Define the rotation animation */
  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }

  /* Initial state */
  .text {
    transform-origin: center;   /* ensure rotation happens around center */
  }

  /* Hover state */
  .bbwm:hover > .text {
    animation: spin 5s linear infinite;  /* spin animation, 2s per full rotation, repeating indefinitely */
  }

</style>
