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
		Yesterday at 3 p.m.,
		Yesterday from 6 till 7,
		When you came
    </TextComment>

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
</template>
