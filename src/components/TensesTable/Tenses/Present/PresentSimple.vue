<script setup>
import Table from '../components/Table.vue';
import TableWrapper from '../components/TableWrapper.vue';
import Row from '../components/Row.vue';

import Col from '../components/Col.vue';
import ColSentence from '../components/ColSentence.vue';
import ColAccent from '../components/ColAccent.vue';
import ColVerb from '../components/ColVerb.vue';

import TextComment from '../components/TextComment.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
    <h2 v-if="details">Present Simple</h2>

    <div class="table" :class="details && 'table-details'">
        <TextComment>
            Usually,
            Often,
            Always,
            Seldom,
            Every day (week, month, year)
        </TextComment>

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
    </div>

    <div v-if="details" class="data-details">
        Data...
    </div>
</template>
