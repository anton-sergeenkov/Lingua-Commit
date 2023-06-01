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
    <h2 v-if="details">Present Perfect Continuous</h2>

    <div class="table" :class="details && 'table-details'">
		<TextComment>
			Since 3 p.m.,
			For a long time,
			For a month
		</TextComment>

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
	</div>

	<div v-if="details" class="data-details">
        Data...
    </div>
</template>
