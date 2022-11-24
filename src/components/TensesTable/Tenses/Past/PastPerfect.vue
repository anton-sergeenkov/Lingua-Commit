<script setup>
import Table from '../components/Table.vue';
import Row from '../components/Row.vue';

import Col from '../components/Col.vue';
import ColSentence from '../components/ColSentence.vue';
import ColAccent from '../components/ColAccent.vue';
import ColVerb from '../components/ColVerb.vue';

import TextComment from '../components/TextComment.vue';
</script>

<template>
    <TextComment>
		Yesterday by 3 p.m.,
		Before some time in the past
    </TextComment>

	<Table>
		<Row>
			<ColSentence>+</ColSentence>
			<ColAccent>*</ColAccent>
			<ColAccent>had</ColAccent>
			<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
		</Row>
	</Table>

	<Table>
		<Row>
			<ColSentence>-</ColSentence>
			<Col>___</Col>
			<ColAccent>hadn't</ColAccent>
			<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
		</Row>
	</Table>

	<Table>
		<Row>
			<ColSentence>?</ColSentence>
			<ColAccent>Had</ColAccent>
			<Col>___</Col>
			<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
		</Row>
	</Table>
</template>
