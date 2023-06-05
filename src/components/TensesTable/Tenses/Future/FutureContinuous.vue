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

import Continuous from '../Continuous.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Future Continuous</h2>

    <div class="table" :class="details && 'table-details'">
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

		<TextComment>
			Tomorrow at 3 p.m.,
			Tomorrow from 6 till 7,
			When you come
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

<!------------------------------------------------------------->
<h4>Виды вопросов</h4>
<!------------------------------------------------------------->
<ul>
    <li><Op>+</Op> <i>I <u>will</u> be eat<u>ing</u> from 5 to 6 tomorrow</i></li>
    <li><Op>-</Op> <i>I <u>won't</u> (will not) be eat<u>ing</u> from 5 to 6 tomorrow</i></li>
    <li><Op>?</Op> <i><u>Will</u> I be eat<u>ing</u> from 5 to 6 tomorrow</i></li>
</ul>

<Continuous />

</div>
</template>
