<script setup>
import Table from '../components/Table.vue';
import TableWrapper from '../components/TableWrapper.vue';
import Row from '../components/Row.vue';

import Col from '../components/Col.vue';
import ColSentence from '../components/ColSentence.vue';
import ColAccent from '../components/ColAccent.vue';
import ColVerb from '../components/ColVerb.vue';

import TextComment from '../components/TextComment.vue';
</script>

<template>
    <TableWrapper>
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
    </TableWrapper>
</template>
