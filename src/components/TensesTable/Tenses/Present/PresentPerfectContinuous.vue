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
    <h2 v-if="details">Present Perfect Continuous</h2>

    <div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence rowspan="2">+</ColSentence>
				<Col>I / You / We / They</Col>
				<ColAccent>have <u>been</u></ColAccent>
				<ColVerb rowspan="3">V<sub>ing</sub></ColVerb>
			</Row>
			<Row>
				<Col>He / She / It</Col>
				<ColAccent>has <u>been</u></ColAccent>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>haven't <u>been</u> / <br/> hasn't <u>been</u></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Have / Has</ColAccent>
				<Col>___ <u>been</u></Col>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<TextComment>
			Since 3 p.m.,
			For a long time,
			For a month
		</TextComment>
	</div>

	<div v-if="details" class="data-details">
        Data...
    </div>
</template>
