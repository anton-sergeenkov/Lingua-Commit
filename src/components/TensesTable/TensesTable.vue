<script setup>
import { dataHeader, dataSide } from './data';

import TableWrapper from './Tenses/components/TableWrapper.vue';

import PresentSimple from './Tenses/Present/PresentSimple.vue';
import PresentContinuous from './Tenses/Present/PresentContinuous.vue';
import PresentPerfect from './Tenses/Present/PresentPerfect.vue';
import PresentPerfectContinuous from './Tenses/Present/PresentPerfectContinuous.vue';

import PastSimple from './Tenses/Past/PastSimple.vue';
import PastContinuous from './Tenses/Past/PastContinuous.vue';
import PastPerfect from './Tenses/Past/PastPerfect.vue';
import PastPerfectContinuous from './Tenses/Past/PastPerfectContinuous.vue';

import FutureSimple from './Tenses/Future/FutureSimple.vue';
import FutureContinuous from './Tenses/Future/FutureContinuous.vue';
import FuturePerfect from './Tenses/Future/FuturePerfect.vue';
import FuturePerfectContinuous from './Tenses/Future/FuturePerfectContinuous.vue';

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
		<TableWrapper style="grid-area: present-s" className="color-present">
			<PresentSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: present-c" className="color-present">
			<PresentContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: present-p" className="color-present">
			<PresentPerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: present-pc" className="color-present">
			<PresentPerfectContinuous />
		</TableWrapper>

		<!-- Past -->
		<TableWrapper style="grid-area: past-s" className="color-past">
			<PastSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: past-c" className="color-past">
			<PastContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: past-p" className="color-past">
			<PastPerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: past-pc" className="color-past">
			<PastPerfectContinuous />
		</TableWrapper>

		<!-- Future -->
		<TableWrapper style="grid-area: future-s" className="color-future">
			<FutureSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: future-c" className="color-future">
			<FutureContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: future-p" className="color-future">
			<FuturePerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: future-pc" className="color-future">
			<FuturePerfectContinuous />
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
		"side-pr  present-s           present-c           present-p           present-pc"
		"side-ps  past-s              past-c              past-p              past-pc"
		"side-ft  future-s            future-c            future-p            future-pc";

	font-size: 15px;
	max-width: 1280px;
	margin: auto;
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
