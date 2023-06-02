<script setup>
import Col from '../../../../uikit/TableElements/Col.vue';
import ColAccent from '../../../../uikit/TableElements/ColAccent.vue';
import ColSentence from '../../../../uikit/TableElements/ColSentence.vue';
import ColVerb from '../../../../uikit/TableElements/ColVerb.vue';
import Row from '../../../../uikit/TableElements/Row.vue';
import Table from '../../../../uikit/TableElements/Table.vue';
import TableWrapper from '../../../../uikit/TableElements/TableWrapper.vue';
import TextComment from '../../../../uikit/TableElements/TextComment.vue';
import TextData from '../../../../uikit/TableElements/TextData.vue';

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

<p>Рутинные, постоянные действия:</p>
<ul>
    <li>Со словами: <em>always</em>, <em>sometimes</em>, <em>usually</em>, <em>often</em>, <em>rarely</em>, <em>never</em>, <em>every day</em> etc.</li>
    <li>С глаголами <em>love</em>, <em>like</em>, <em>hate</em>, <em>want</em>, <em>need</em>, <em>believe</em> etc.</li>
</ul>

<p>Глагол To Be - это "быть".</p>
<p>"Am / Is / Are" - формы глагола To Be в Present Simple</p>

<h4>1. To Be: Am / Is / Are</h4>
<p><b></b></p>
<ul>
    <li><s>✔</s> I am a developer</li>
    <li><s>✖</s> I am not a developer</li>
    <li><s>?</s> Am I a developer?</li>
</ul>

<h4>2. Modals Verb (Can, Must, May)</h4>
<ul>
    <li><s>✔</s> I can swim</li>
    <li><s>✖</s> I can’t swim</li>
    <li><s>?</s> Can I swim?</li>
</ul>

<h4>3. Verb: Do / Does</h4>
<ul>
    <li><s>✔</s> I drink wine</li>
    <li><s>✖</s> I don’t drink wine</li>
    <li><s>?</s> Do I drink wine?</li>
</ul>

<ul>
    <li><s>✔</s> She drinks wine</li>
    <li><s>✖</s> She doesn’t drink wine</li>
    <li><s>?</s> Does she drink wine?</li>
</ul>

</div>
</template>
