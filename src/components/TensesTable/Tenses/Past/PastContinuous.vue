<script setup>
import Col from '@/uikit/TableElements/Col.vue';
import ColAccent from '@/uikit/TableElements/ColAccent.vue';
import ColSentence from '@/uikit/TableElements/ColSentence.vue';
import ColVerb from '@/uikit/TableElements/ColVerb.vue';
import Row from '@/uikit/TableElements/Row.vue';
import Table from '@/uikit/TableElements/Table.vue';
import TableWrapper from '@/uikit/TableElements/TableWrapper.vue';
import TextComment from '@/uikit/TableElements/TextComment.vue';
import TextData from '@/uikit/TableElements/TextData.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Past Continuous</h2>

	<div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence rowspan="2">+</ColSentence>
				<Col>I / He / She / It </Col>
				<ColAccent>was</ColAccent>
				<ColVerb rowspan="2">V<sub>ing</sub></ColVerb>
			</Row>
			<Row>
				<Col>You / We / They </Col>
				<ColAccent>were</ColAccent>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>wasn't / weren't</ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Was / Were</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>
		<TextComment>
			Yesterday at 3 p.m.,
			Yesterday from 6 till 7,
			When you came
		</TextComment>
	</div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
