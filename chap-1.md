# Chapter 1
# Building Abstractions with Procedures
<script src="https://github.com/snap-blocks/snapblocks/releases/download/v1.8.1/snapblocks.min.js"></script>
<pre class="blocks">
forever {
    move ((distance to [mouse-cursor V]) / 50) steps
    turn towards [mouse-cursor V]
}
</pre>