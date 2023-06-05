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

import Op from '@/uikit/Options.vue';
import Info from '@/uikit/Info.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
    <h2 v-if="details">Future Simple</h2>

    <div class="table" :class="details && 'table-details'">
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

		<TextComment>
			Tomorrow,
			Next week (month, year)
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

<ul>
	<li><mark>Will be</mark> - формы глагола ToBe во Future Simple</li>
	<li>Не используются модальные глаголы: <em>Can</em>, <em>Must</em>, <em>May</em></li>
</ul>

<!------------------------------------------------------------->
<h4>Виды вопросов</h4>
<!------------------------------------------------------------->
<h5>ToBe: Will be</h5>
<ul>
    <li><Op>+</Op> <i>I <u>will</u> drink wine</i></li>
    <li><Op>-</Op> <i>I <u>won't</u> (will not) drink wine</i></li>
    <li><Op>?</Op> <i><u>Will</u> I drink wine?</i></li>
</ul>

<!------------------------------------------------------------->
<h4>Shall</h4>
<!------------------------------------------------------------->
<ul>
	<li><mark>Shall</mark> используется, если что-то вежливо предлагается</li>
	<li><i>Shall I help you?</i></li>
</ul>

</div>
</template>
