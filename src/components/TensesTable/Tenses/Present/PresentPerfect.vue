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
    <h2 v-if="details">Present Perfect</h2>

    <div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence rowspan="2">+</ColSentence>
				<Col>I / You / We / They</Col>
				<ColAccent>have</ColAccent>
				<ColVerb rowspan="3">V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
			<Row>
				<Col>He / She / It </Col>
				<ColAccent>has</ColAccent>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>haven't / hasn't</ColAccent>
				<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Have / Has</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>3</sub> / V<sub>ed</sub></ColVerb>
			</Row>
		</Table>

		<TextComment>
			Ever,
			Never,
			Just,
			Already,
			Not … yet,
			By 3 p.m.
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

<ul>
	<li>Действие просто произошло</li>
	<li><em>This</em>, <em>That</em>, <em>These</em>, <em>Those</em></li>
</ul>

<!------------------------------------------------------------->
<h4>Виды вопросов</h4>
<!------------------------------------------------------------->
<ul>
    <li><Op>+</Op> <i>I <s>have</s> eaten fish</i></li>
    <li><Op>-</Op> <i>I <s>haven’t</s> eaten fish</i></li>
    <li><Op>?</Op> <i><s>Have</s> I eaten fish?</i></li>
</ul>

<!------------------------------------------------------------->
<h4>Сокращения</h4>
<!------------------------------------------------------------->
<ul>
	<li><em>I have</em> been = <em>I’ve</em> been</li>
	<li><em>He has</em> been = <em>He’s</em> been</li>
</ul>
</div>
</template>
