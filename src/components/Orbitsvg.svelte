<!-- <script>
  import { spring } from 'svelte/motion';

  let isOpen = false;
  function toggleOrbit() {
    isOpen = !isOpen;
    console.log(isOpen)
  }

  let width = spring(0);
  $: if (isOpen) {
    width.set(80);  // Set the spring target to 100
  } else {
    width.set(0);  // Set the spring target to 0
  }

</script>

<div class="orbit-bracket">
  <div class="brackets" on:click={toggleOrbit}>
    <svg width="50" height="780" viewBox="0 280 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M31.72 1050H1V1H31.72" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    </svg>
  </div>
  <div class="orbit-container" style="width: {$width}vw;">
    <svg viewbox="0 400 1876 1800" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M932.12 895.04C1052.66 895.04 1150.37 869.041 1150.37 836.97C1150.37 804.899 1052.66 778.9 932.12 778.9C811.584 778.9 713.87 804.899 713.87 836.97C713.87 869.041 811.584 895.04 932.12 895.04Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M932.72 1463.25C1224.61 1463.25 1461.23 1401.17 1461.23 1324.6C1461.23 1248.03 1224.61 1185.95 932.72 1185.95C640.832 1185.95 404.21 1248.03 404.21 1324.6C404.21 1401.17 640.832 1463.25 932.72 1463.25Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M931.87 1716.23C1191.03 1716.23 1401.12 1661.12 1401.12 1593.13C1401.12 1525.14 1191.03 1470.03 931.87 1470.03C672.71 1470.03 462.62 1525.14 462.62 1593.13C462.62 1661.12 672.71 1716.23 931.87 1716.23Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M929.81 1085.34C1159.01 1085.34 1344.82 1036.6 1344.82 976.47C1344.82 916.342 1159.01 867.6 929.81 867.6C700.606 867.6 514.8 916.342 514.8 976.47C514.8 1036.6 700.606 1085.34 929.81 1085.34Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M931.35 1856.42C1051.89 1856.42 1149.6 1830.42 1149.6 1798.35C1149.6 1766.28 1051.89 1740.28 931.35 1740.28C810.814 1740.28 713.1 1766.28 713.1 1798.35C713.1 1830.42 810.814 1856.42 931.35 1856.42Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M668.05 1761.09C816.565 1761.09 936.96 1564.57 936.96 1322.14C936.96 1079.71 816.565 883.19 668.05 883.19C519.535 883.19 399.14 1079.71 399.14 1322.14C399.14 1564.57 519.535 1761.09 668.05 1761.09Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M1202.54 1761.71C1351.05 1761.71 1471.45 1565.19 1471.45 1322.76C1471.45 1080.33 1351.05 883.81 1202.54 883.81C1054.03 883.81 933.63 1080.33 933.63 1322.76C933.63 1565.19 1054.03 1761.71 1202.54 1761.71Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M820.66 1846.98C884.891 1846.98 936.96 1610.77 936.96 1319.4C936.96 1028.03 884.891 791.82 820.66 791.82C756.429 791.82 704.36 1028.03 704.36 1319.4C704.36 1610.77 756.429 1846.98 820.66 1846.98Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M1043.61 1479.96C1277.44 1296.75 1416.53 1083.83 1354.28 1004.39C1292.04 924.947 1052.02 1009.07 818.198 1192.28C584.373 1375.49 445.282 1588.41 507.528 1667.85C569.775 1747.29 809.787 1663.17 1043.61 1479.96Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M398.55 1321.35L1460.65 1322.17" stroke="white" stroke-miterlimit="10"/>
    <path d="M815.14 1850.33L815.96 788.23" stroke="white" stroke-miterlimit="10"/>
    <path d="M1054.9 1844.28C1119.13 1844.28 1171.2 1608.07 1171.2 1316.7C1171.2 1025.33 1119.13 789.12 1054.9 789.12C990.669 789.12 938.6 1025.33 938.6 1316.7C938.6 1608.07 990.669 1844.28 1054.9 1844.28Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M822.63 1187.45C1056.44 1004.23 1292.28 920.94 1354.53 1000.38C1376.29 1028.15 1377.62 1071.38 1354.73 1124.8C1338.15 1163.51 1311.04 1207.11 1275.14 1252.98" stroke="white" stroke-width="9" stroke-miterlimit="10"/>
    <path d="M1063.87 1889.52L1064.69 827.42" stroke="white" stroke-miterlimit="10"/>
    <path d="M938.88 892.88C821.02 892.88 725.13 796.99 725.13 679.13C725.13 622.03 747.36 568.36 787.74 527.98C828.12 487.6 881.79 465.37 938.89 465.37C995.99 465.37 1049.66 487.6 1090.04 527.98C1130.42 568.36 1152.65 622.03 1152.65 679.13C1152.65 796.99 1056.76 892.88 938.9 892.88H938.88Z" fill="black"/>
    <path d="M969.42 835C969.13 835.06 968.84 835.11 968.55 835.17C958.94 836.99 949.02 837.95 938.88 837.95C927.01 837.95 915.43 836.64 904.3 834.16M908.56 523.19C908.87 523.13 909.19 523.07 909.5 523.01C919.09 521.23 928.92 520.31 938.89 520.31C948.86 520.31 958.94 521.25 968.65 523.08C968.79 523.11 968.92 523.13 969.06 523.16M832.68 708.6L1042.96 708.66M833.41 649.67L1042.46 650.42M971.1 577.48C987.4 582.69 1002.33 591.75 1014.78 604.2C1035.33 624.75 1046.65 652.08 1046.65 681.15C1046.65 729.35 1015.15 770.33 971.66 784.59L971.82 834.5C1043.64 819.29 1097.7 755.4 1097.7 679.12C1097.7 636.7 1081.18 596.82 1051.18 566.82C1029.21 544.85 1000.8 530.33 971.1 524.01V577.48ZM906.65 576.42C890.27 581.62 873.37 591.04 860.87 603.54C840.32 624.09 829 651.42 829 680.49C829 728.27 859.95 768.95 902.85 783.55L902.98 833.84C832.64 817.52 780.07 754.35 780.07 679.12C780.07 636.7 796.59 596.82 826.59 566.82C848.56 544.85 875.85 530.1 905.54 523.79C905.82 523.73 906.11 523.67 906.39 523.61L906.65 576.41V576.42ZM938.88 892.88C821.02 892.88 725.13 796.99 725.13 679.13C725.13 622.03 747.36 568.36 787.74 527.98C828.12 487.6 881.79 465.37 938.89 465.37C995.99 465.37 1049.66 487.6 1090.04 527.98C1130.42 568.36 1152.65 622.03 1152.65 679.13C1152.65 796.99 1056.76 892.88 938.9 892.88H938.88Z" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="884.15" y="737.56">UNCONSCIOUS</tspan></text>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="908.66" y="684.55">CENSOR</tspan></text>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="875.72" y="632.96">CONSCIOUSNESS</tspan></text>
    <text transform="translate(1054.53 600.09) rotate(56.31)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">S</tspan></text>
    <text transform="translate(1060.55 609.151) rotate(60.75)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">H</tspan></text>
    <text transform="translate(1065.96 619.023) rotate(63.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(1068.06 623.176) rotate(66.82)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(1072.07 632.609) rotate(70.81)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(1075.32 641.948) rotate(75.08)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">D</tspan></text>
    <text transform="translate(1079.29 657.989) rotate(81.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">O</tspan></text>
    <text transform="translate(1081.02 670.801) rotate(86.45)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">F</tspan></text>
    <text transform="translate(1081.66 685.359) rotate(92.52)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">R</tspan></text>
    <text transform="translate(1081.15 696.206) rotate(96.76)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(1079.92 706.461) rotate(101.19)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">A</tspan></text>
    <text transform="translate(1077.58 717.981) rotate(105.51)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(1074.94 727.25) rotate(108.34)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(1073.52 731.567) rotate(110.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">T</tspan></text>
    <text transform="translate(1069.88 741.048) rotate(115.29)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">Y</tspan></text>
    <text transform="translate(812.735 755.046) rotate(-117.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">S</tspan></text>
    <text transform="translate(807.72 745.378) rotate(-113.07)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">H</tspan></text>
    <text transform="translate(803.406 734.988) rotate(-109.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(801.765 730.623) rotate(-106.99)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(798.804 720.814) rotate(-103)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(796.573 711.194) rotate(-98.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">D</tspan></text>
    <text transform="translate(794.358 694.794) rotate(-91.85)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">O</tspan></text>
    <text transform="translate(794.037 681.848) rotate(-87.28)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">F</tspan></text>
    <text transform="translate(794.986 667.331) rotate(-81.22)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">R</tspan></text>
    <text transform="translate(796.674 656.626) rotate(-77)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(798.996 646.575) rotate(-72.6)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">A</tspan></text>
    <text transform="translate(802.562 635.23) rotate(-67.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(806.196 626.429) rotate(-65.54)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(808.084 622.173) rotate(-62.67)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">T</tspan></text>
    <text transform="translate(812.709 613.235) rotate(-58.51)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">Y</tspan></text>
    <g class="disc">
      <path d="M317.77 1481.78C199.91 1481.78 104.02 1385.89 104.02 1268.03C104.02 1210.93 126.25 1157.26 166.63 1116.88C207.01 1076.5 260.68 1054.27 317.78 1054.27C374.88 1054.27 428.55 1076.5 468.93 1116.88C509.31 1157.26 531.54 1210.93 531.54 1268.03C531.54 1385.89 435.65 1481.78 317.79 1481.78H317.77Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="futurisms" cx="317.77" cy="1268.02" r="193.75" fill="#3DAF37" />
      <text transform="translate(71.9655 1148.56) rotate(-61.06)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(86.271 1123.44) rotate(-56.44)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(94.5011 1111.11) rotate(-53.34)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(103.48 1099.17) rotate(-50.63)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(110.769 1090.16) rotate(-47.24)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">c</tspan></text>
      <text transform="translate(125.622 1074.19) rotate(-42.6)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(142.78 1058.54) rotate(-37.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">n</tspan></text>
      <text transform="translate(161.944 1044.04) rotate(-33.55)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(174.625 1035.56) rotate(-29.57)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(194.628 1024.44) rotate(-25.56)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">t</tspan></text>
      <text transform="translate(208.503 1017.73) rotate(-21.54)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(229.823 1009.55) rotate(-17.62)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(242.946 1005.45) rotate(-15.11)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(253.041 1002.64) rotate(-11.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(274.081 998.023) rotate(-6.09)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M669.25 2057.75C551.39 2057.75 455.5 1961.86 455.5 1844C455.5 1786.9 477.73 1733.23 518.11 1692.85C558.49 1652.47 612.16 1630.24 669.26 1630.24C726.36 1630.24 780.03 1652.47 820.41 1692.85C860.79 1733.23 883.02 1786.9 883.02 1844C883.02 1961.86 787.13 2057.75 669.27 2057.75H669.25Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="nowism" cx="668.55" cy="1843.55" r="197.55" fill="#AC8FAD" />
      <text transform="translate(491.761 1982.62) rotate(51.93)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(507.2 2001.98) rotate(46.84)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(515.391 2010.78) rotate(43.39)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(523.923 2019.17) rotate(38.81)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(539.494 2031.78) rotate(33.26)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">n</tspan></text>
      <text transform="translate(555.235 2042.24) rotate(27.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(572.557 2051.69) rotate(21.18)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">w</tspan></text>
      <text transform="translate(597.987 2061.13) rotate(16.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(605.045 2063.43) rotate(12.93)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(620.855 2067.56) rotate(6.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M1534.7 1492.34C1416.84 1492.34 1320.95 1396.45 1320.95 1278.59C1320.95 1221.49 1343.18 1167.82 1383.56 1127.44C1423.94 1087.06 1477.61 1064.83 1534.71 1064.83C1591.81 1064.83 1645.48 1087.06 1685.86 1127.44C1726.24 1167.82 1748.47 1221.49 1748.47 1278.59C1748.47 1396.45 1652.58 1492.34 1534.72 1492.34H1534.7Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="futurism" cx="1535.45" cy="1278.68" r="196.62" fill="#61A485" />
      <text transform="translate(1617.46 1013.59) rotate(19.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(1644.6 1023.68) rotate(24.35)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1658.11 1029.84) rotate(27.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1672.05 1037.01) rotate(31.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1692.38 1049.82) rotate(35.73)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1704.8 1058.68) rotate(39.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(1722.24 1073.38) rotate(43.53)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">t</tspan></text>
      <text transform="translate(1733.41 1083.92) rotate(47.48)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(1748.69 1100.87) rotate(51.36)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1757.21 1111.66) rotate(53.86)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1763.48 1120.08) rotate(57.08)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1775.35 1138.1) rotate(62.99)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M940.28 1486.16C822.42 1486.16 726.53 1390.27 726.53 1272.41C726.53 1215.31 748.76 1161.64 789.14 1121.26C829.52 1080.88 883.19 1058.65 940.29 1058.65C997.39 1058.65 1051.06 1080.88 1091.44 1121.26C1131.82 1161.64 1154.05 1215.31 1154.05 1272.41C1154.05 1390.27 1058.16 1486.16 940.3 1486.16H940.28Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1091.02 1468.17C1050.37 1499.6 999.41 1518.33 944.17 1518.33C888.93 1518.33 842.51 1501.24 802.81 1472.29" stroke="black" stroke-width="44.55" stroke-miterlimit="10"/>
      <text transform="translate(839.156 1466.42) rotate(26.47)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(861.44 1477.28) rotate(21.39)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(872.627 1481.71) rotate(17.97)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(883.949 1485.61) rotate(13.41)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(903.468 1490.32) rotate(7.98)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(921.558 1492.96) rotate(2.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">p</tspan></text>
      <text transform="translate(940.731 1493.96) rotate(-2.96)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(960.792 1492.94) rotate(-8.27)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">c</tspan></text>
      <text transform="translate(978.002 1490.54) rotate(-13.31)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(996.231 1486.07) rotate(-16.84)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">l</tspan></text>
      <text transform="translate(1002.75 1484.36) rotate(-20.56)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">p</tspan></text>
      <text transform="translate(1020.86 1477.6) rotate(-25.67)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1036.04 1470.41) rotate(-30.62)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">e</tspan></text>
      <circle class="apocalypse" cx="940.02" cy="1270.75" r="195.385" fill="#742BC1" />
    </g>
    <g class="disc">
      <path d="M1245.34 2037.81C1127.48 2037.81 1031.59 1941.92 1031.59 1824.06C1031.59 1766.96 1053.82 1713.29 1094.2 1672.91C1134.58 1632.53 1188.25 1610.3 1245.35 1610.3C1302.45 1610.3 1356.12 1632.53 1396.5 1672.91C1436.88 1713.29 1459.11 1766.96 1459.11 1824.06C1459.11 1941.92 1363.22 2037.81 1245.36 2037.81H1245.34Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <text transform="translate(1275.3 2040.11) rotate(-9.26)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(1299.71 2035.91) rotate(-14.43)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1311.34 2032.95) rotate(-17.9)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1322.8 2029.49) rotate(-22.49)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1341.39 2021.82) rotate(-27.77)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">v</tspan></text>
      <text transform="translate(1356.69 2013.92) rotate(-33.01)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1373.83 2002.58) rotate(-36.94)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1380.01 1998.23) rotate(-40.71)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">d</tspan></text>
      <text transform="translate(1394.66 1985.42) rotate(-44.48)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1400.23 1980.21) rotate(-47.97)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1411.52 1968.4) rotate(-54.37)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
      <circle class="voidism" cx="1245.57" cy="1821.75" r="194.16" fill="#765383" />
    </g>
    <g class="arrows">
      <path d="M468.96 1729.18C467.63 1727.69 466.31 1726.19 464.99 1724.68M457.04 1715.4C406.35 1655.1 366.73 1585.17 341.33 1508.76" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M337.06 1524.93L336.33 1494.04C336.33 1493.67 336.8 1493.51 337.01 1493.82L354.9 1519.79C355.09 1520.07 354.81 1520.43 354.49 1520.32L343.76 1516.41L337.8 1525.15C337.58 1525.48 337.06 1525.33 337.05 1524.93H337.06Z" fill="white"/>
      <path d="M1044.31 1932.07C1042.34 1932.4 1040.36 1932.71 1038.39 1933.02M1026.64 1934.74C998.4 1938.6 969.57 1940.6 940.28 1940.6C923.51 1940.6 906.89 1939.95 890.45 1938.66" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M902.89 1948.91L874.39 1936.98C874.05 1936.84 874.1 1936.33 874.47 1936.27L905.48 1930.52C905.81 1930.46 906.03 1930.86 905.79 1931.11L897.85 1939.31L903.4 1948.32C903.61 1948.66 903.26 1949.07 902.89 1948.91Z" fill="white"/>
      <path d="M1459.63 1683.64L1434.77 1701.99C1434.47 1702.21 1434.07 1701.91 1434.2 1701.56L1445.17 1671.99C1445.29 1671.67 1445.75 1671.69 1445.84 1672.02L1448.81 1683.04L1459.39 1682.9C1459.79 1682.9 1459.96 1683.4 1459.64 1683.64H1459.63Z" fill="white"/>
      <path d="M1533 1526.55C1511.58 1585.04 1481.76 1639.47 1444.99 1688.38M1538.93 1509.63C1538.3 1511.53 1537.65 1513.42 1537 1515.31" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1173.89 723.22C1175.75 723.96 1177.6 724.71 1179.45 725.47M1190.48 730.12C1329.19 790.09 1442.11 898.41 1508.01 1033.83" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1509.57 1015.83L1514.44 1046.34C1514.5 1046.71 1514.04 1046.93 1513.79 1046.65L1492.58 1023.31C1492.35 1023.06 1492.58 1022.66 1492.91 1022.73L1504.06 1025.16L1508.8 1015.7C1508.98 1015.34 1509.51 1015.43 1509.57 1015.82V1015.83Z" fill="white"/>
      <path d="M371.63 1035.72C372.5 1033.92 373.38 1032.12 374.26 1030.33M379.82 1019.35C447.3 889.31 558.71 785.74 694.39 728.27" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M682.97 722.92L713.78 720.63C714.15 720.6 714.33 721.07 714.04 721.3L689 740.48C688.73 740.69 688.35 740.42 688.45 740.1L691.81 729.19L682.78 723.68C682.44 723.47 682.57 722.95 682.96 722.92H682.97Z" fill="white"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="1423.89" y="800.406">Black</tspan></text>
      <path class="circle" d="M1396.01 831.36C1399.99 831.36 1403.22 828.132 1403.22 824.15C1403.22 820.168 1399.99 816.94 1396.01 816.94C1392.03 816.94 1388.8 820.168 1388.8 824.15C1388.8 828.132 1392.03 831.36 1396.01 831.36Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="1577.99" y="1656.08">Beyond</tspan></text>
      <path class="circle" d="M1538.83 1632.16C1542.81 1632.16 1546.04 1628.93 1546.04 1624.95C1546.04 1620.97 1542.81 1617.74 1538.83 1617.74C1534.85 1617.74 1531.62 1620.97 1531.62 1624.95C1531.62 1628.93 1534.85 1632.16 1538.83 1632.16Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="259.55" y="1693.32">Warp</tspan></text>
      <path class="circle" d="M367.5 1671.75C371.482 1671.75 374.71 1668.52 374.71 1664.54C374.71 1660.56 371.482 1657.33 367.5 1657.33C363.518 1657.33 360.29 1660.56 360.29 1664.54C360.29 1668.52 363.518 1671.75 367.5 1671.75Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="336.33" y="800.406">Mode</tspan></text>
      <path class="circle" d="M450.55 837.94C454.532 837.94 457.76 834.711 457.76 830.729C457.76 826.748 454.532 823.52 450.55 823.52C446.568 823.52 443.34 826.748 443.34 830.729C443.34 834.711 446.568 837.94 450.55 837.94Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    </svg>
  </div>
  <div class="brackets" on:click={toggleOrbit}>
    <svg width="50" height="780" viewBox="-18 280 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0.27002 1050H31V1.62012H0.27002" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    </svg>
  </div>
</div>

<style>
  svg {
    width: 70%;
  }

  .orbit-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .orbit-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }

  .circle:hover {
    fill: white;
  }

  .disc:hover > .futurism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 1535.45px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .futurisms {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 317.77px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .apocalypse {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 940.02px center;  /* Center of the circle */
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .nowism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 668.55px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .voidism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 1245.57px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

</style> -->

<script>
  import { spring } from 'svelte/motion';
  import inView from './inView.js'

  let animate = false;
  let isOpen = false;

  let animationOrder = 'forward';  // initial value
  let width = spring(0, {stiffness: 0.05, damping: 0.8});
  $: if (isOpen) {
    width.set(90);  // Set the spring target to 90
  } else {
    width.set(0);  // Set the spring target to 0
  }

  function handleAnimationEnd(event) {
    if (event.propertyName === 'height' && event.target.dataset.bracket === 'right') {
      const elementHeight = event.target.clientHeight;
      if (elementHeight > 100) {
        isOpen = true;
      }
    }
  }

</script>

<div class="orbit-bracket"
  use:inView={{ threshold: 0.9}}
  on:enter={() => {
    animationOrder = 'forward';
    animate = true;
    console.log('animate');
    console.log(animate);
  }}
  on:exit={() => {
    animationOrder = 'reverse'
    isOpen = false;
    console.log('is Open');
    console.log(isOpen);
    animate = false;
    console.log('animate');
    console.log(animate);
  }}>
  <div class="shape-left {animationOrder}" class:animate={animate} data-bracket="left"></div>
  <div class="orbit-container" style="width: {$width}vw;">
    <svg viewbox="0 400 1876 1800" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M932.12 895.04C1052.66 895.04 1150.37 869.041 1150.37 836.97C1150.37 804.899 1052.66 778.9 932.12 778.9C811.584 778.9 713.87 804.899 713.87 836.97C713.87 869.041 811.584 895.04 932.12 895.04Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M932.72 1463.25C1224.61 1463.25 1461.23 1401.17 1461.23 1324.6C1461.23 1248.03 1224.61 1185.95 932.72 1185.95C640.832 1185.95 404.21 1248.03 404.21 1324.6C404.21 1401.17 640.832 1463.25 932.72 1463.25Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M931.87 1716.23C1191.03 1716.23 1401.12 1661.12 1401.12 1593.13C1401.12 1525.14 1191.03 1470.03 931.87 1470.03C672.71 1470.03 462.62 1525.14 462.62 1593.13C462.62 1661.12 672.71 1716.23 931.87 1716.23Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M929.81 1085.34C1159.01 1085.34 1344.82 1036.6 1344.82 976.47C1344.82 916.342 1159.01 867.6 929.81 867.6C700.606 867.6 514.8 916.342 514.8 976.47C514.8 1036.6 700.606 1085.34 929.81 1085.34Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M931.35 1856.42C1051.89 1856.42 1149.6 1830.42 1149.6 1798.35C1149.6 1766.28 1051.89 1740.28 931.35 1740.28C810.814 1740.28 713.1 1766.28 713.1 1798.35C713.1 1830.42 810.814 1856.42 931.35 1856.42Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M668.05 1761.09C816.565 1761.09 936.96 1564.57 936.96 1322.14C936.96 1079.71 816.565 883.19 668.05 883.19C519.535 883.19 399.14 1079.71 399.14 1322.14C399.14 1564.57 519.535 1761.09 668.05 1761.09Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M1202.54 1761.71C1351.05 1761.71 1471.45 1565.19 1471.45 1322.76C1471.45 1080.33 1351.05 883.81 1202.54 883.81C1054.03 883.81 933.63 1080.33 933.63 1322.76C933.63 1565.19 1054.03 1761.71 1202.54 1761.71Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M820.66 1846.98C884.891 1846.98 936.96 1610.77 936.96 1319.4C936.96 1028.03 884.891 791.82 820.66 791.82C756.429 791.82 704.36 1028.03 704.36 1319.4C704.36 1610.77 756.429 1846.98 820.66 1846.98Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M1043.61 1479.96C1277.44 1296.75 1416.53 1083.83 1354.28 1004.39C1292.04 924.947 1052.02 1009.07 818.198 1192.28C584.373 1375.49 445.282 1588.41 507.528 1667.85C569.775 1747.29 809.787 1663.17 1043.61 1479.96Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M398.55 1321.35L1460.65 1322.17" stroke="white" stroke-miterlimit="10"/>
    <path d="M815.14 1850.33L815.96 788.23" stroke="white" stroke-miterlimit="10"/>
    <path d="M1054.9 1844.28C1119.13 1844.28 1171.2 1608.07 1171.2 1316.7C1171.2 1025.33 1119.13 789.12 1054.9 789.12C990.669 789.12 938.6 1025.33 938.6 1316.7C938.6 1608.07 990.669 1844.28 1054.9 1844.28Z" stroke="white" stroke-miterlimit="10"/>
    <path d="M822.63 1187.45C1056.44 1004.23 1292.28 920.94 1354.53 1000.38C1376.29 1028.15 1377.62 1071.38 1354.73 1124.8C1338.15 1163.51 1311.04 1207.11 1275.14 1252.98" stroke="white" stroke-width="9" stroke-miterlimit="10"/>
    <path d="M1063.87 1889.52L1064.69 827.42" stroke="white" stroke-miterlimit="10"/>
    <path d="M938.88 892.88C821.02 892.88 725.13 796.99 725.13 679.13C725.13 622.03 747.36 568.36 787.74 527.98C828.12 487.6 881.79 465.37 938.89 465.37C995.99 465.37 1049.66 487.6 1090.04 527.98C1130.42 568.36 1152.65 622.03 1152.65 679.13C1152.65 796.99 1056.76 892.88 938.9 892.88H938.88Z" fill="black"/>
    <path d="M969.42 835C969.13 835.06 968.84 835.11 968.55 835.17C958.94 836.99 949.02 837.95 938.88 837.95C927.01 837.95 915.43 836.64 904.3 834.16M908.56 523.19C908.87 523.13 909.19 523.07 909.5 523.01C919.09 521.23 928.92 520.31 938.89 520.31C948.86 520.31 958.94 521.25 968.65 523.08C968.79 523.11 968.92 523.13 969.06 523.16M832.68 708.6L1042.96 708.66M833.41 649.67L1042.46 650.42M971.1 577.48C987.4 582.69 1002.33 591.75 1014.78 604.2C1035.33 624.75 1046.65 652.08 1046.65 681.15C1046.65 729.35 1015.15 770.33 971.66 784.59L971.82 834.5C1043.64 819.29 1097.7 755.4 1097.7 679.12C1097.7 636.7 1081.18 596.82 1051.18 566.82C1029.21 544.85 1000.8 530.33 971.1 524.01V577.48ZM906.65 576.42C890.27 581.62 873.37 591.04 860.87 603.54C840.32 624.09 829 651.42 829 680.49C829 728.27 859.95 768.95 902.85 783.55L902.98 833.84C832.64 817.52 780.07 754.35 780.07 679.12C780.07 636.7 796.59 596.82 826.59 566.82C848.56 544.85 875.85 530.1 905.54 523.79C905.82 523.73 906.11 523.67 906.39 523.61L906.65 576.41V576.42ZM938.88 892.88C821.02 892.88 725.13 796.99 725.13 679.13C725.13 622.03 747.36 568.36 787.74 527.98C828.12 487.6 881.79 465.37 938.89 465.37C995.99 465.37 1049.66 487.6 1090.04 527.98C1130.42 568.36 1152.65 622.03 1152.65 679.13C1152.65 796.99 1056.76 892.88 938.9 892.88H938.88Z" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="884.15" y="737.56">UNCONSCIOUS</tspan></text>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="908.66" y="684.55">CENSOR</tspan></text>
    <text fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" letter-spacing="0em"><tspan x="875.72" y="632.96">CONSCIOUSNESS</tspan></text>
    <text transform="translate(1054.53 600.09) rotate(56.31)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">S</tspan></text>
    <text transform="translate(1060.55 609.151) rotate(60.75)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">H</tspan></text>
    <text transform="translate(1065.96 619.023) rotate(63.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(1068.06 623.176) rotate(66.82)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(1072.07 632.609) rotate(70.81)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(1075.32 641.948) rotate(75.08)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">D</tspan></text>
    <text transform="translate(1079.29 657.989) rotate(81.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">O</tspan></text>
    <text transform="translate(1081.02 670.801) rotate(86.45)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">F</tspan></text>
    <text transform="translate(1081.66 685.359) rotate(92.52)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">R</tspan></text>
    <text transform="translate(1081.15 696.206) rotate(96.76)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(1079.92 706.461) rotate(101.19)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">A</tspan></text>
    <text transform="translate(1077.58 717.981) rotate(105.51)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(1074.94 727.25) rotate(108.34)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(1073.52 731.567) rotate(110.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">T</tspan></text>
    <text transform="translate(1069.88 741.048) rotate(115.29)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">Y</tspan></text>
    <text transform="translate(812.735 755.046) rotate(-117.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">S</tspan></text>
    <text transform="translate(807.72 745.378) rotate(-113.07)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">H</tspan></text>
    <text transform="translate(803.406 734.988) rotate(-109.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(801.765 730.623) rotate(-106.99)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(798.804 720.814) rotate(-103)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(796.573 711.194) rotate(-98.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">D</tspan></text>
    <text transform="translate(794.358 694.794) rotate(-91.85)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">O</tspan></text>
    <text transform="translate(794.037 681.848) rotate(-87.28)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">F</tspan></text>
    <text transform="translate(794.986 667.331) rotate(-81.22)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">R</tspan></text>
    <text transform="translate(796.674 656.626) rotate(-77)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">E</tspan></text>
    <text transform="translate(798.996 646.575) rotate(-72.6)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">A</tspan></text>
    <text transform="translate(802.562 635.23) rotate(-67.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">L</tspan></text>
    <text transform="translate(806.196 626.429) rotate(-65.54)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">I</tspan></text>
    <text transform="translate(808.084 622.173) rotate(-62.67)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">T</tspan></text>
    <text transform="translate(812.709 613.235) rotate(-58.51)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="15" font-weight="600" letter-spacing="0em"><tspan x="0" y="13.14">Y</tspan></text>
    <g class="disc">
      <path d="M317.77 1481.78C199.91 1481.78 104.02 1385.89 104.02 1268.03C104.02 1210.93 126.25 1157.26 166.63 1116.88C207.01 1076.5 260.68 1054.27 317.78 1054.27C374.88 1054.27 428.55 1076.5 468.93 1116.88C509.31 1157.26 531.54 1210.93 531.54 1268.03C531.54 1385.89 435.65 1481.78 317.79 1481.78H317.77Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="futurisms" cx="317.77" cy="1268.02" r="193.75" fill="#3DAF37" />
      <text transform="translate(71.9655 1148.56) rotate(-61.06)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(86.271 1123.44) rotate(-56.44)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(94.5011 1111.11) rotate(-53.34)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(103.48 1099.17) rotate(-50.63)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(110.769 1090.16) rotate(-47.24)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">c</tspan></text>
      <text transform="translate(125.622 1074.19) rotate(-42.6)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(142.78 1058.54) rotate(-37.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">n</tspan></text>
      <text transform="translate(161.944 1044.04) rotate(-33.55)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(174.625 1035.56) rotate(-29.57)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(194.628 1024.44) rotate(-25.56)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">t</tspan></text>
      <text transform="translate(208.503 1017.73) rotate(-21.54)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(229.823 1009.55) rotate(-17.62)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(242.946 1005.45) rotate(-15.11)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(253.041 1002.64) rotate(-11.91)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(274.081 998.023) rotate(-6.09)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M669.25 2057.75C551.39 2057.75 455.5 1961.86 455.5 1844C455.5 1786.9 477.73 1733.23 518.11 1692.85C558.49 1652.47 612.16 1630.24 669.26 1630.24C726.36 1630.24 780.03 1652.47 820.41 1692.85C860.79 1733.23 883.02 1786.9 883.02 1844C883.02 1961.86 787.13 2057.75 669.27 2057.75H669.25Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="nowism" cx="668.55" cy="1843.55" r="197.55" fill="#AC8FAD" />
      <text transform="translate(491.761 1982.62) rotate(51.93)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(507.2 2001.98) rotate(46.84)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(515.391 2010.78) rotate(43.39)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(523.923 2019.17) rotate(38.81)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(539.494 2031.78) rotate(33.26)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">n</tspan></text>
      <text transform="translate(555.235 2042.24) rotate(27.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(572.557 2051.69) rotate(21.18)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">w</tspan></text>
      <text transform="translate(597.987 2061.13) rotate(16.72)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(605.045 2063.43) rotate(12.93)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(620.855 2067.56) rotate(6.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M1534.7 1492.34C1416.84 1492.34 1320.95 1396.45 1320.95 1278.59C1320.95 1221.49 1343.18 1167.82 1383.56 1127.44C1423.94 1087.06 1477.61 1064.83 1534.71 1064.83C1591.81 1064.83 1645.48 1087.06 1685.86 1127.44C1726.24 1167.82 1748.47 1221.49 1748.47 1278.59C1748.47 1396.45 1652.58 1492.34 1534.72 1492.34H1534.7Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <circle class="futurism" cx="1535.45" cy="1278.68" r="196.62" fill="#61A485" />
      <text transform="translate(1617.46 1013.59) rotate(19.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(1644.6 1023.68) rotate(24.35)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1658.11 1029.84) rotate(27.5)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1672.05 1037.01) rotate(31.65)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1692.38 1049.82) rotate(35.73)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1704.8 1058.68) rotate(39.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(1722.24 1073.38) rotate(43.53)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">t</tspan></text>
      <text transform="translate(1733.41 1083.92) rotate(47.48)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">u</tspan></text>
      <text transform="translate(1748.69 1100.87) rotate(51.36)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1757.21 1111.66) rotate(53.86)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1763.48 1120.08) rotate(57.08)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1775.35 1138.1) rotate(62.99)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
    </g>
    <g class="disc">
      <path d="M940.28 1486.16C822.42 1486.16 726.53 1390.27 726.53 1272.41C726.53 1215.31 748.76 1161.64 789.14 1121.26C829.52 1080.88 883.19 1058.65 940.29 1058.65C997.39 1058.65 1051.06 1080.88 1091.44 1121.26C1131.82 1161.64 1154.05 1215.31 1154.05 1272.41C1154.05 1390.27 1058.16 1486.16 940.3 1486.16H940.28Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1091.02 1468.17C1050.37 1499.6 999.41 1518.33 944.17 1518.33C888.93 1518.33 842.51 1501.24 802.81 1472.29" stroke="black" stroke-width="44.55" stroke-miterlimit="10"/>
      <text transform="translate(839.156 1466.42) rotate(26.47)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(861.44 1477.28) rotate(21.39)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(872.627 1481.71) rotate(17.97)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(883.949 1485.61) rotate(13.41)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(903.468 1490.32) rotate(7.98)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(921.558 1492.96) rotate(2.64)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">p</tspan></text>
      <text transform="translate(940.731 1493.96) rotate(-2.96)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(960.792 1492.94) rotate(-8.27)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">c</tspan></text>
      <text transform="translate(978.002 1490.54) rotate(-13.31)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">a</tspan></text>
      <text transform="translate(996.231 1486.07) rotate(-16.84)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">l</tspan></text>
      <text transform="translate(1002.75 1484.36) rotate(-20.56)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">p</tspan></text>
      <text transform="translate(1020.86 1477.6) rotate(-25.67)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1036.04 1470.41) rotate(-30.62)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">e</tspan></text>
      <circle class="apocalypse" cx="940.02" cy="1270.75" r="195.385" fill="#742BC1" />
    </g>
    <g class="disc">
      <path d="M1245.34 2037.81C1127.48 2037.81 1031.59 1941.92 1031.59 1824.06C1031.59 1766.96 1053.82 1713.29 1094.2 1672.91C1134.58 1632.53 1188.25 1610.3 1245.35 1610.3C1302.45 1610.3 1356.12 1632.53 1396.5 1672.91C1436.88 1713.29 1459.11 1766.96 1459.11 1824.06C1459.11 1941.92 1363.22 2037.81 1245.36 2037.81H1245.34Z" fill="black" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <text transform="translate(1275.3 2040.11) rotate(-9.26)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">A</tspan></text>
      <text transform="translate(1299.71 2035.91) rotate(-14.43)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">f</tspan></text>
      <text transform="translate(1311.34 2032.95) rotate(-17.9)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">r</tspan></text>
      <text transform="translate(1322.8 2029.49) rotate(-22.49)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="600" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1341.39 2021.82) rotate(-27.77)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">v</tspan></text>
      <text transform="translate(1356.69 2013.92) rotate(-33.01)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">o</tspan></text>
      <text transform="translate(1373.83 2002.58) rotate(-36.94)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1380.01 1998.23) rotate(-40.71)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">d</tspan></text>
      <text transform="translate(1394.66 1985.42) rotate(-44.48)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">i</tspan></text>
      <text transform="translate(1400.23 1980.21) rotate(-47.97)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">s</tspan></text>
      <text transform="translate(1411.52 1968.4) rotate(-54.37)" fill="white" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" letter-spacing="0em"><tspan x="0" y="31.436">m</tspan></text>
      <circle class="voidism" cx="1245.57" cy="1821.75" r="194.16" fill="#765383" />
    </g>
    <g class="arrows">
      <path d="M468.96 1729.18C467.63 1727.69 466.31 1726.19 464.99 1724.68M457.04 1715.4C406.35 1655.1 366.73 1585.17 341.33 1508.76" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M337.06 1524.93L336.33 1494.04C336.33 1493.67 336.8 1493.51 337.01 1493.82L354.9 1519.79C355.09 1520.07 354.81 1520.43 354.49 1520.32L343.76 1516.41L337.8 1525.15C337.58 1525.48 337.06 1525.33 337.05 1524.93H337.06Z" fill="white"/>
      <path d="M1044.31 1932.07C1042.34 1932.4 1040.36 1932.71 1038.39 1933.02M1026.64 1934.74C998.4 1938.6 969.57 1940.6 940.28 1940.6C923.51 1940.6 906.89 1939.95 890.45 1938.66" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M902.89 1948.91L874.39 1936.98C874.05 1936.84 874.1 1936.33 874.47 1936.27L905.48 1930.52C905.81 1930.46 906.03 1930.86 905.79 1931.11L897.85 1939.31L903.4 1948.32C903.61 1948.66 903.26 1949.07 902.89 1948.91Z" fill="white"/>
      <path d="M1459.63 1683.64L1434.77 1701.99C1434.47 1702.21 1434.07 1701.91 1434.2 1701.56L1445.17 1671.99C1445.29 1671.67 1445.75 1671.69 1445.84 1672.02L1448.81 1683.04L1459.39 1682.9C1459.79 1682.9 1459.96 1683.4 1459.64 1683.64H1459.63Z" fill="white"/>
      <path d="M1533 1526.55C1511.58 1585.04 1481.76 1639.47 1444.99 1688.38M1538.93 1509.63C1538.3 1511.53 1537.65 1513.42 1537 1515.31" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1173.89 723.22C1175.75 723.96 1177.6 724.71 1179.45 725.47M1190.48 730.12C1329.19 790.09 1442.11 898.41 1508.01 1033.83" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M1509.57 1015.83L1514.44 1046.34C1514.5 1046.71 1514.04 1046.93 1513.79 1046.65L1492.58 1023.31C1492.35 1023.06 1492.58 1022.66 1492.91 1022.73L1504.06 1025.16L1508.8 1015.7C1508.98 1015.34 1509.51 1015.43 1509.57 1015.82V1015.83Z" fill="white"/>
      <path d="M371.63 1035.72C372.5 1033.92 373.38 1032.12 374.26 1030.33M379.82 1019.35C447.3 889.31 558.71 785.74 694.39 728.27" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <path d="M682.97 722.92L713.78 720.63C714.15 720.6 714.33 721.07 714.04 721.3L689 740.48C688.73 740.69 688.35 740.42 688.45 740.1L691.81 729.19L682.78 723.68C682.44 723.47 682.57 722.95 682.96 722.92H682.97Z" fill="white"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="1423.89" y="800.406">Black</tspan></text>
      <path class="circle" d="M1396.01 831.36C1399.99 831.36 1403.22 828.132 1403.22 824.15C1403.22 820.168 1399.99 816.94 1396.01 816.94C1392.03 816.94 1388.8 820.168 1388.8 824.15C1388.8 828.132 1392.03 831.36 1396.01 831.36Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="1577.99" y="1656.08">Beyond</tspan></text>
      <path class="circle" d="M1538.83 1632.16C1542.81 1632.16 1546.04 1628.93 1546.04 1624.95C1546.04 1620.97 1542.81 1617.74 1538.83 1617.74C1534.85 1617.74 1531.62 1620.97 1531.62 1624.95C1531.62 1628.93 1534.85 1632.16 1538.83 1632.16Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="259.55" y="1693.32">Warp</tspan></text>
      <path class="circle" d="M367.5 1671.75C371.482 1671.75 374.71 1668.52 374.71 1664.54C374.71 1660.56 371.482 1657.33 367.5 1657.33C363.518 1657.33 360.29 1660.56 360.29 1664.54C360.29 1668.52 363.518 1671.75 367.5 1671.75Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    <g class="circle">
      <text fill="white" stroke="white" stroke-miterlimit="10" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="36" font-weight="300" letter-spacing="0em"><tspan x="336.33" y="800.406">Mode</tspan></text>
      <path class="circle" d="M450.55 837.94C454.532 837.94 457.76 834.711 457.76 830.729C457.76 826.748 454.532 823.52 450.55 823.52C446.568 823.52 443.34 826.748 443.34 830.729C443.34 834.711 446.568 837.94 450.55 837.94Z" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
    </g>
    </svg>
  </div>
  <div class="shape-right {animationOrder}" class:animate={animate} data-bracket="right" on:transitionend={handleAnimationEnd}></div>
</div>

<style>
  svg {
    width: 70%;
  }

  .orbit-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 95vw;
    height: 95vh;
    overflow: hidden;
  }

  .orbit-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    width: 80vw;
    height: 80vh;
    /* border: 1px dashed #aaa; */
  }

  /* .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  } */

  .circle:hover {
    fill: white;
  }

  .disc:hover > .futurism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 1535.45px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .futurisms {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 317.77px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .apocalypse {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 940.02px center;  /* Center of the circle */
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .nowism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 668.55px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .disc:hover > .voidism {
    transition: transform 0.3s;  /* Smooth transition */
    transform-origin: 1245.57px center;
    transform: rotateY(180deg);  /* Rotate by 45 degrees around the Z-axis */
  }

  .shape-left{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    width: 50px;
    height: 100px;
    border: 2px solid white;
    border-right: none;
    background-color: transparent;

    transform-origin: center;
    transform: rotate(-45deg) translateY(17.666%) translateX(-15%);
  }

  .shape-right{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    width: 50px;
    height: 100px;
    border: 2px solid white;
    border-left: none;
    background-color: transparent;

    transform-origin: center;
    transform: rotate(-45deg) translateY(-17.666%) translateX(15%);
  }

  .shape-left.forward, .shape-right.forward {
    transition:
        transform 1s,
        height 1s 1s;
  }

  .shape-left.reverse, .shape-right.reverse {
    transition:
        height 1s 1s,
        transform 1s 1s;
  }

  .shape-left.animate {
    transform: rotate(0deg) translateY(0%) translateX(0%);
    height: 80vh;
  }

  .shape-right.animate {
    transform: rotate(0deg) translateY(0%) translateX(0%);
    height: 80vh;
  }

</style>
