<script setup>
import { dataHeader, dataSide } from './data';

import PresentSimple from './Tenses/Present/PresentSimple.vue';
import PresentContinuous from './Tenses/Present/PresentContinuous.vue';
import PresentPerfect from './Tenses/Present/PresentPerfect.vue';
import PresentPerfectContinuous from './Tenses/Present/PresentPerfectContinuous.vue';

import TableWrapper from './Tenses/components/TableWrapper.vue';
</script>

<template>
	<div class="container">
		<div class="item" :style="'grid-area: clear'"></div>

		<!-- Header -->
		<div
			v-text="item.name"
			v-for="(item, key) in dataHeader"
			:style="'grid-area: '+item.grid+'-name'"
			class="item header"
			:key="key+'-name'"
		/>
		<div
			v-text="item.question"
			v-for="(item, key) in dataHeader"
			:style="'grid-area: '+item.grid+'-question'"
			class="item subheader"
			:key="key+'-question'"
		/>
		<div
			v-text="item.description"
			v-for="(item, key) in dataHeader"
			:style="'grid-area: '+item.grid+'-text'"
			class="item comment"
			:key="key+'-text'"
		/>

		<!-- Side -->
		<div
			v-text="item.name"
			v-for="(item, key) in dataSide"
			:style="'grid-area: '+item.grid"
			class="item header"
			:key="key"
		/>

		<!-- Present -->
		<TableWrapper style="grid-area: ps" className="color-present">
			<PresentSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: pc" className="color-present">
			<PresentContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: pp" className="color-present">
			<PresentPerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: ppc" className="color-present">
			<PresentPerfectContinuous />
		</TableWrapper>
	</div>
</template>

<style>
u {
	background-color: #e5e1eb;
	padding: 1px;
	border-radius: 3px;
	text-decoration: none;
	color: #595959;
	font-weight: 600;
}
</style>

<style scoped>
.color-present {
	background-color: #e1edd3;
}
.color-past {
	background-color: #ede9d3;
}
.color-future {
	background-color: #d3e9ed;
}

.container {
    display: grid;
	gap: 1px;
    grid-template-columns: repeat(5, auto);
    grid-template-areas:
        "clear    header-sl-name      header-cs-name      header-pt-name      header-pc-name"
        "clear    header-sl-question  header-cs-question  header-pt-question  header-pc-question"
        "clear    header-sl-text      header-cs-text      header-pt-text      header-pc-text"
		"side-pr  ps                  pc                  pp                  ppc"
		"side-ps  . . . ."
		"side-ft  . . . .";

	font-size: 15px;
    border: 1px solid rgba(0,0,0,.1);
    background-color: rgba(0,0,0,.25);
	box-shadow:  var(--box-shadow-container);
}

.item {
	padding: 9px;
	background-color: #fff;
}
.header {
	display: flex;
	justify-content: center;
	align-items: center;
	padding: 15px;
	font-weight: 700;
	text-align: center;
}
.subheader {
	display: flex;
	justify-content: center;
	align-items: center;
	font-size: 13px;
	font-weight: 700;
	text-align: center;
	color: var(--color-blue);
}
.comment {
	display: flex;
	justify-content: center;
	align-items: center;
	font-size: 13px;
	text-align: center;
	font-style: italic;
	color: var(--color-gray-dark);
}
</style>
