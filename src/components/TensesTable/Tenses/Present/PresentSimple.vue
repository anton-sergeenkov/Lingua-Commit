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
    <h2 v-if="details">Present Simple</h2>

    <div class="table" :class="details && 'table-details'">
        <Table>
            <Row>
                <ColSentence rowspan="2">+</ColSentence>
                <Col>I / You / We / They</Col>
                <ColVerb>V<sub>1</sub></ColVerb>
            </Row>
            <Row>
                <Col>He / She / It</Col>
                <ColVerb>V<sub>s</sub></ColVerb>
            </Row>
        </Table>

        <Table>
            <Row>
                <ColSentence>-</ColSentence>
                <Col>___</Col>
                <ColAccent>don't / doesn't</ColAccent>
                <ColVerb>V<sub>1</sub></ColVerb>
            </Row>
        </Table>

        <Table>
            <Row>
                <ColSentence>?</ColSentence>
                <ColAccent>Do / Does</ColAccent>
                <Col>___</Col>
                <ColVerb>V<sub>1</sub></ColVerb>
            </Row>
        </Table>

        <TextComment>
            Usually,
            Often,
            Always,
            Seldom,
            Every day (week, month, year)
        </TextComment>
    </div>

<div v-if="details" class="data-details">

<hr />

<!------------------------------------------------------------->
<h4>Основные слова</h4>
<!------------------------------------------------------------->
<ul>
    <li>Рутинные, постоянные действия</li>
    <li>Со словами: <em>always</em>, <em>sometimes</em>, <em>usually</em>, <em>often</em>, <em>rarely</em>, <em>never</em>, <em>every day</em> etc.</li>
    <li>С глаголами <em>love</em>, <em>like</em>, <em>hate</em>, <em>want</em>, <em>need</em>, <em>believe</em> etc.</li>
</ul>

<!------------------------------------------------------------->
<h4>3 вида глаголов</h4>
<!------------------------------------------------------------->
<Info>
<ul>
    <li>3 вида глаголов только для Present Simple и Past Simple</li>
    <li>Глагол To Be - это "быть"</li>
    <li>"Am / Is / Are" - формы глагола To Be в Present Simple</li>
</ul>
</Info>

<h5>1. To Be: Am / Is / Are</h5>
<p><b></b></p>
<ul>
    <li><Op>+</Op> I am a developer</li>
    <li><Op>-</Op> I am not a developer</li>
    <li><Op>?</Op> Am I a developer?</li>
</ul>

<h5>2. Modals Verb (Can, Must, May)</h5>
<ul>
    <li><Op>+</Op> I can swim</li>
    <li><Op>-</Op> I can’t swim</li>
    <li><Op>?</Op> Can I swim?</li>
</ul>

<h5>3. Verb: Do / Does</h5>
<ul>
    <li><Op>+</Op> I drink wine</li>
    <li><Op>-</Op> I don’t drink wine</li>
    <li><Op>?</Op> Do I drink wine?</li>
</ul>
<ul>
    <li><Op>+</Op> She drinks wine</li>
    <li><Op>-</Op> She doesn’t drink wine</li>
    <li><Op>?</Op> Does she drink wine?</li>
</ul>

</div>
</template>
