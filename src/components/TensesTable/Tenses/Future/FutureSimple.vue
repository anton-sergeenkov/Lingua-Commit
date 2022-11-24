<script setup>
import Table from '../components/Table.vue';
import Row from '../components/Row.vue';

import Col from '../components/Col.vue';
import ColSentence from '../components/ColSentence.vue';
import ColAccent from '../components/ColAccent.vue';
import ColVerb from '../components/ColVerb.vue';

import TextComment from '../components/TextComment.vue';
import TextData from '../components/TextData.vue';
</script>

<template>
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
</template>
