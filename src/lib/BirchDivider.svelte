<!-- 
  BirchDivider.svelte
  Subtle SVG birch branch decoration used as a section divider.
  Inline SVG — no external image dependencies.
-->
<script>
  /** Optional CSS class overrides */
  let { class: cls = '' } = $props();
</script>

<svg
  class="birch-divider {cls}"
  viewBox="0 0 600 32"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
  aria-hidden="true"
>
  <!-- Main horizontal branch -->
  <path d="M0 16 Q150 10 300 16 Q450 22 600 16" stroke="#4a7c59" stroke-width="1.5" fill="none" stroke-linecap="round"/>
  
  <!-- Left side twigs -->
  <path d="M80 14 Q90 6 105 4" stroke="#4a7c59" stroke-width="1" fill="none" stroke-linecap="round"/>
  <path d="M80 14 Q88 18 100 22" stroke="#4a7c59" stroke-width="0.8" fill="none" stroke-linecap="round"/>
  <path d="M140 13 Q150 5 162 2" stroke="#4a7c59" stroke-width="0.8" fill="none" stroke-linecap="round"/>
  
  <!-- Small leaves on twigs -->
  <ellipse cx="105" cy="4" rx="5" ry="3" fill="#8ab89a" opacity="0.7" transform="rotate(-20 105 4)"/>
  <ellipse cx="100" cy="22" rx="4" ry="2.5" fill="#8ab89a" opacity="0.6" transform="rotate(15 100 22)"/>
  <ellipse cx="162" cy="2" rx="4" ry="2.5" fill="#8ab89a" opacity="0.65" transform="rotate(-30 162 2)"/>

  <!-- Center decorative mark -->
  <circle cx="300" cy="16" r="3" fill="#4a7c59" opacity="0.5"/>
  
  <!-- Right side twigs -->
  <path d="M420 17 Q432 8 448 6" stroke="#4a7c59" stroke-width="0.8" fill="none" stroke-linecap="round"/>
  <path d="M420 17 Q430 24 444 27" stroke="#4a7c59" stroke-width="0.8" fill="none" stroke-linecap="round"/>
  <path d="M480 16 Q492 7 506 5" stroke="#4a7c59" stroke-width="1" fill="none" stroke-linecap="round"/>
  
  <!-- Right leaves -->
  <ellipse cx="448" cy="6" rx="5" ry="2.5" fill="#8ab89a" opacity="0.65" transform="rotate(-25 448 6)"/>
  <ellipse cx="444" cy="27" rx="4" ry="2.5" fill="#8ab89a" opacity="0.6" transform="rotate(20 444 27)"/>
  <ellipse cx="506" cy="5" rx="4.5" ry="2.5" fill="#8ab89a" opacity="0.7" transform="rotate(-20 506 5)"/>
</svg>
