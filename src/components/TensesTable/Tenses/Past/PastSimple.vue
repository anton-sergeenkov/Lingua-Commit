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
	<h2 v-if="details">Past Simple</h2>

	<div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<ColAccent>*</ColAccent>
				<ColVerb>V<sub>2</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>didn't</ColAccent>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Did</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>1</sub></ColVerb>
			</Row>
		</Table>

		<TextComment>
			Yesterday,
			Last week (month, year),
			Long ago
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

<ul>
	<li>Действие произошло в конкретное время</li>
	<li><mark>Was</mark> / <mark>Were</mark> - формы глагола ToBe в Past Simple</li>
</ul>

<!------------------------------------------------------------->
<h4>3 вида глаголов</h4>
<!------------------------------------------------------------->
<Info>
<ul>
    <li>3 вида глаголов только для Present Simple и Past Simple</li>
    <li><em>YOU</em> - мн.ч.</li>
</ul>
</Info>

<Info>
<ul>
    <li>Глагол To Be - это "быть"</li>
    <li>Используется если нет действия / глагола</li>
</ul>
</Info>

<h5>1. ToBe: <em>Was</em> (ед. ч.) / <em>Were</em> (мн.ч.)</h5>
<ul>
	<li>I / He / She / It - <mark>was</mark></li>
	<li>You / We / They - <mark>were</mark></li>
</ul>

<ul>
    <li><Op>+</Op> <i>I <u>was</u> a developer a month ago</i></li>
    <li><Op>-</Op> <i>I <u>wasn’t</u> a developer a month ago</i></li>
    <li><Op>?</Op> <i><u>Was</u> I a developer a month ago?</i></li>
    <li><Op>?</Op> <i>Why <u>were</u> you angry yesterday?</i> (you - мн.ч.)</li>
</ul>

<h5>2. Modals Verb: <em>Can</em>, <em>Must</em>, <em>May</em></h5>
<ul>
    <li><Op>+</Op> <i>I <u>could</u> swim</i></li>
    <li><Op>-</Op> <i>I <u>couldn’t</u> swim</i></li>
    <li><Op>?</Op> <i><u>Could</u> I swim?</i></li>
</ul>

<h5>3. Verb: <em>Did</em></h5>
<ul>
    <li><Op>+</Op> <i>I drank wine</i></li>
    <li><Op>-</Op> <i>I <u>didn’t</u> drink wine</i></li>
    <li><Op>?</Op> <i><u>Did</u> I drink wine?</i></li>
</ul>

</div>
</template>
