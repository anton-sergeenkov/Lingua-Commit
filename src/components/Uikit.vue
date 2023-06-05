<script setup>
import Op from '@/uikit/Options.vue';
import Info from '@/uikit/Info.vue';
import TwoSides from '@/uikit/TwoSides.vue';
</script>

<template>
  <h2>Ui-Kit</h2>

<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<h3>Tags</h3>
<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<ul>
    <li><b>&lt;b&gt;</b></li>
    <li><u>&lt;u&gt;</u></li>
    <li><i>&lt;i&gt;</i></li>
    <li><em>&lt;em&gt;</em></li>
    <li><s>&lt;s&gt;</s></li>
    <li><mark>&lt;mark&gt;</mark></li>
</ul>

<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<h3>Info</h3>
<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<pre><code>
import Info from '@/uikit/Info.vue';

&lt;Info&gt;
    &lt;ul&gt;
        &lt;li&gt;Hello1&lt;/li&gt;
        &lt;li&gt;Hello2&lt;/li&gt;
    &lt;/ul&gt;
&lt;/Info&gt;
</code></pre>

<Info>
    <ul>
        <li>Hello1</li>
        <li>Hello2</li>
    </ul>
</Info>

<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<h3>Options</h3>
<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<pre><code>
import Op from '@/uikit/Options.vue';

&lt;Op&gt;+&lt;/Op&gt;
&lt;Op&gt;-&lt;/Op&gt;
&lt;Op&gt;?&lt;/Op&gt;
</code></pre>

<Op>+</Op>
<Op>-</Op>
<Op>?</Op>

<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<h3>TwoSides</h3>
<!-- xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -->
<pre><code>
import TwoSides from '@/uikit/TwoSides.vue';

&lt;TwoSides&gt;
    &lt;template v-slot:first&gt;
        Content1
    &lt;/template&gt;
    &lt;template v-slot:last&gt;
        Content2
    &lt;/template&gt;
&lt;/TwoSides&gt;
</code></pre>

</template>
