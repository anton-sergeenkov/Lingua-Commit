<script setup>
import { ref } from 'vue';

import { dataHeader, dataSide } from './data';

import TableWrapper from '../../uikit/TableElements/TableWrapper.vue';

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

function getDescription(arg) {
    isTableView.value = false;
	currentTense.value = arg;
}

const isTableView = ref(true);
const currentTense = ref('');
</script>

<template>
	<div class="container" v-if="isTableView">
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
		<TableWrapper style="grid-area: present-s" className="color-present" @click="getDescription('PresentSimple')">
			<PresentSimple  />
		</TableWrapper>
		<TableWrapper style="grid-area: present-c" className="color-present" @click="getDescription('PresentContinuous')">
			<PresentContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: present-p" className="color-present" @click="getDescription('PresentPerfect')">
			<PresentPerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: present-pc" className="color-present" @click="getDescription('PresentPerfectContinuous')">
			<PresentPerfectContinuous />
		</TableWrapper>

		<!-- Past -->
		<TableWrapper style="grid-area: past-s" className="color-past" @click="getDescription('PastSimple')">
			<PastSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: past-c" className="color-past" @click="getDescription('PastContinuous')">
			<PastContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: past-p" className="color-past" @click="getDescription('PastPerfect')">
			<PastPerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: past-pc" className="color-past" @click="getDescription('PastPerfectContinuous')">
			<PastPerfectContinuous />
		</TableWrapper>

		<!-- Future -->
		<TableWrapper style="grid-area: future-s" className="color-future" @click="getDescription('FutureSimple')">
			<FutureSimple />
		</TableWrapper>
		<TableWrapper style="grid-area: future-c" className="color-future" @click="getDescription('FutureContinuous')">
			<FutureContinuous />
		</TableWrapper>
		<TableWrapper style="grid-area: future-p" className="color-future" @click="getDescription('FuturePerfect')">
			<FuturePerfect />
		</TableWrapper>
		<TableWrapper style="grid-area: future-pc" className="color-future" @click="getDescription('FuturePerfectContinuous')">
			<FuturePerfectContinuous />
		</TableWrapper>
	</div>
	<div v-else class="details-wrapper">
		<button class="details-close" @click="isTableView = !isTableView">🏷️</button>

		<PresentSimple details v-if="currentTense === 'PresentSimple'" />
		<PresentContinuous details v-if="currentTense === 'PresentContinuous'" />
		<PresentPerfect details v-if="currentTense === 'PresentPerfect'" />
		<PresentPerfectContinuous details v-if="currentTense === 'PresentPerfectContinuous'" />

		<PastSimple details v-if="currentTense === 'PastSimple'" />
		<PastContinuous details v-if="currentTense === 'PastContinuous'" />
		<PastPerfect details v-if="currentTense === 'PastPerfect'" />
		<PastPerfectContinuous details v-if="currentTense === 'PastPerfectContinuous'" />

		<FutureSimple details v-if="currentTense === 'FutureSimple'" />
		<FutureContinuous details v-if="currentTense === 'FutureContinuous'" />
		<FuturePerfect details v-if="currentTense === 'FuturePerfect'" />
		<FuturePerfectContinuous details v-if="currentTense === 'FuturePerfectContinuous'" />
	</div>
</template>

<style scoped>
/***************************************************
Structure
/***************************************************/
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
    border: 1px solid rgba(0,0,0,.09);
    background-color: rgba(0,0,0,.15);
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
	text-align: center;
	font-family: Roboto-Medium;
}
.subheader {
	display: flex;
	justify-content: center;
	align-items: center;
	font-size: 13px;
	text-align: center;
	color: rgb(var(--color-violet-blue));
	font-family: Roboto-Medium;
}
.comment {
	display: flex;
	justify-content: center;
	align-items: center;
	font-size: 13px;
	text-align: center;
	font-family: Roboto-Italic;
	color: rgb(var(--color-gray-70));
}

/***************************************************
Tenses Block
/***************************************************/
.color-present,
.color-past,
.color-future {
	transition: .4s;
	cursor: pointer;
	outline: 2px solid transparent;
}

.color-present { background-color: #e1edd3; }
.color-past    { background-color: #ede9d3; }
.color-future  { background-color: #d3e9ed; }

.color-present:hover,
.color-past:hover,
.color-future:hover {
	filter: brightness(90%);
	outline: 1px solid rgba(0,0,0,.3);
}

/***************************************************
Details
/***************************************************/
.details-wrapper {
	max-width: 1280px;
	margin: auto;
    background-color: #fff;
    box-shadow:  var(--box-shadow-container);
    padding: 10px 30px;
}
.details-close {
	width: 40px;
	height: 40px;
	display: block;
	font-size: 18px;
	cursor: pointer;
	border-radius: 50%;
	border: none;
	background: none;
	background-color: rgba(0,0,0,.1);
	margin-bottom: 10px;
}
</style>
