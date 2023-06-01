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
	<h2 v-if="details">Future Perfect Continuous</h2>

	<div class="table" :class="details && 'table-details'">
		<TextComment>
			Tomorrow since 3 p.m.,
			For some time in the future
		</TextComment>

		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<Col>___</Col>
				<ColAccent>will have <u>been</u></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>won't have <u>been</u></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Will</ColAccent>
				<ColAccent>___ have <u>been</u></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
