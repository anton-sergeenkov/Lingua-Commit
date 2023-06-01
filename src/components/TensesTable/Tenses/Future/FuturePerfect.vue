<script setup>
import Table from '../components/Table.vue';
import Row from '../components/Row.vue';

import Col from '../components/Col.vue';
import ColSentence from '../components/ColSentence.vue';
import ColAccent from '../components/ColAccent.vue';
import ColVerb from '../components/ColVerb.vue';

import TextComment from '../components/TextComment.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Future Perfect</h2>

	<div class="table" :class="details && 'table-details'">
		<TextComment>
			Tomorrow by 3 p.m.,
			By some time in the future
		</TextComment>

		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<ColAccent>*</ColAccent>
				<ColAccent>will <u>have</u></ColAccent>
				<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>won't <u>have</u></ColAccent>
				<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Will</ColAccent>
				<ColAccent>___ <u>have</u></ColAccent>
				<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
