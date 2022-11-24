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
		Tomorrow at 3 p.m.,
		Tomorrow from 6 till 7,
		When you come
    </TextComment>

	<Table>
		<Row>
			<ColSentence>+</ColSentence>
			<ColAccent>*</ColAccent>
			<ColAccent>will <u>be</u></ColAccent>
			<ColVerb>V<sub>ing</sub></ColVerb>
		</Row>
	</Table>

	<Table>
		<Row>
			<ColSentence>-</ColSentence>
			<Col>___</Col>
			<ColAccent>won't <u>be</u></ColAccent>
			<ColVerb>V<sub>ing</sub></ColVerb>
		</Row>
	</Table>

	<Table>
		<Row>
			<ColSentence>?</ColSentence>
			<ColAccent>Will</ColAccent>
			<ColAccent>___ <u>be</u></ColAccent>
			<ColVerb>V<sub>ing</sub></ColVerb>
		</Row>
	</Table>
</template>
