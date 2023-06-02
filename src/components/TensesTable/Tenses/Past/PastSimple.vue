<script setup>
import Col from '../../../../uikit/TableElements/Col.vue';
import ColAccent from '../../../../uikit/TableElements/ColAccent.vue';
import ColSentence from '../../../../uikit/TableElements/ColSentence.vue';
import ColVerb from '../../../../uikit/TableElements/ColVerb.vue';
import Row from '../../../../uikit/TableElements/Row.vue';
import Table from '../../../../uikit/TableElements/Table.vue';
import TableWrapper from '../../../../uikit/TableElements/TableWrapper.vue';
import TextComment from '../../../../uikit/TableElements/TextComment.vue';
import TextData from '../../../../uikit/TableElements/TextData.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Past Simple</h2>

	<div class="table" :class="details && 'table-details'">
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

		<TextComment>
			Yesterday,
			Last week (month, year),
			Long ago
		</TextComment>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
