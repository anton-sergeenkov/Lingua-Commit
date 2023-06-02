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
