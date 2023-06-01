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
	<h2 v-if="details">Past Simple</h2>

	<div class="table" :class="details && 'table-details'">
		<TextComment>
			Yesterday,
			Last week (month, year),
			Long ago
		</TextComment>

		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<ColAccent>*</ColAccent>
				<ColVerb>V<sub>2</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>didn't</ColAccent>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Did</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
