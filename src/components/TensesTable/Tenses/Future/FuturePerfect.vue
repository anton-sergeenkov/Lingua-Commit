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
