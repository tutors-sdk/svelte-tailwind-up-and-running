<script lang="ts">
	import ModeSwitcher from './ModeSwitcher.svelte';
	import Tailwindcss from './Tailwindcss.svelte';
	import A_SettingUp from './pages/A_SettingUp.svelte'
	import B_UtilityFirst from './pages/B_UtilityFirst.svelte'
	import C_ResponsiveDesign from './pages/C_ResponsiveDesign.svelte'
	import D_HoverFocus from './pages/D_HoverFocus.svelte'
	import E_ComposingUtilities from './pages/E_ComposingUtilities.svelte'
	import F_ExtractingComponents from './pages/F_ExtractingComponents.svelte'
	import Router from "svelte-spa-router";

	let routes = {
		"/a-setting-up": A_SettingUp,
		"/b-utility-first" : B_UtilityFirst,
		"/c-responsive-design" : C_ResponsiveDesign,
		"/d-hover-focus" : D_HoverFocus,
		"/e-composing-utilities" : E_ComposingUtilities,
		"/f-extracting-components" : F_ExtractingComponents
	};

</script>
<style>
	.custom-style {
		@apply italic;
	}
</style>
<Tailwindcss />
<ModeSwitcher />

<ol>
	<li> <a href="/#/a-setting-up"> Setting Up </a></li>
	<li> <a href="/#/b-utility-first"> Utility First </a></li>
	<li> <a href="/#/c-responsive-design"> Responsive Design </a></li>
	<li> <a href="/#/d-hover-focus"> Hover Focus </a></li>
	<li> <a href="/#/e-composing-utilities"> Composing Utilities </a></li>
	<li> <a href="/#/f-extracting-components"> Extracting Components </a></li>
</ol>

<Router {routes} restoreScrollState={true} />
