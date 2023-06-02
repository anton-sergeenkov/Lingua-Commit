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
    <h2 v-if="details">Future Simple</h2>

    <div class="table" :class="details && 'table-details'">
		<TextComment>
			Tomorrow,
			Next week (month, year)
		</TextComment>

		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<ColAccent>*</ColAccent>
				<ColAccent>will</ColAccent>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>

		<TextData>will = 'll</TextData>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>won't</ColAccent>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>

		<TextData>will not = won't</TextData>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Will</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
