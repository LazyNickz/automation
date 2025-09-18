
<?xml version="1.0" encoding="UTF-8"?>
<bpmn:definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:bpmn="http://www.omg.org/spec/BPMN/20100524/MODEL" xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI" xmlns:dc="http://www.omg.org/spec/DD/20100524/DC" xmlns:di="http://www.omg.org/spec/DD/20100524/DI" id="Definitions_0xi5fmu" targetNamespace="http://bpmn.io/schema/bpmn" exporter="bpmn-js (https://demo.bpmn.io)" exporterVersion="18.6.1">
  <bpmn:collaboration id="Collaboration_0l6ul9b">
    <bpmn:participant id="Participant_0p3g1rl" name="creator" processRef="Process_1axdosu" />
    <bpmn:participant id="Participant_1bna06k" name="google sheets" processRef="Process_0wcxzi5" />
    <bpmn:participant id="Participant_0hubn45" name="LLM" processRef="Process_11gzt64" />
    <bpmn:participant id="Participant_0xrni4t" name="FLUX image generator" processRef="Process_0m6ibzc" />
    <bpmn:participant id="Participant_0qib768" name="kling img to vid" processRef="Process_1auvgky" />
    <bpmn:participant id="Participant_1y5125u" name="elevenlabs" processRef="Process_1yn7l45" />
    <bpmn:participant id="Participant_0ktswqz" name="creatomate" processRef="Process_0cah0cf" />
    <bpmn:participant id="Participant_1qnspw5" name="google drive" processRef="Process_0irng22" />
    <bpmn:messageFlow id="Flow_13txqb1" sourceRef="Activity_0czh9p7" targetRef="Activity_022ndt8" />
    <bpmn:messageFlow id="Flow_1pfxenp" sourceRef="Activity_022ndt8" targetRef="Activity_085ulwn" />
    <bpmn:messageFlow id="Flow_11dwuw0" sourceRef="Activity_022ndt8" targetRef="Activity_1je3r2b" />
    <bpmn:messageFlow id="Flow_1koptz8" sourceRef="Activity_085ulwn" targetRef="Activity_1me3o3i" />
    <bpmn:messageFlow id="Flow_0t182xq" sourceRef="Activity_1me3o3i" targetRef="Activity_16qhb17" />
    <bpmn:messageFlow id="Flow_0gp79au" sourceRef="Activity_085ulwn" targetRef="Activity_16qhb17" />
    <bpmn:messageFlow id="Flow_1ftuigg" sourceRef="Activity_085ulwn" targetRef="Activity_1yajq2o" />
    <bpmn:messageFlow id="Flow_15sgib1" sourceRef="Activity_16qhb17" targetRef="Activity_0bl3gqg" />
    <bpmn:messageFlow id="Flow_1chlh2j" sourceRef="Activity_1yajq2o" targetRef="Activity_0bl3gqg" />
    <bpmn:messageFlow id="Flow_09b9734" sourceRef="Activity_1je3r2b" targetRef="Activity_0bl3gqg" />
    <bpmn:messageFlow id="Flow_0b9qu4h" sourceRef="Activity_0rfaq6y" targetRef="Activity_0tg4iy1" />
    <bpmn:messageFlow id="Flow_1wmq128" sourceRef="Activity_0tg4iy1" targetRef="Activity_13hbii9" />
  </bpmn:collaboration>
  <bpmn:process id="Process_1axdosu" isExecutable="false">
    <bpmn:startEvent id="StartEvent_159a0qr">
      <bpmn:outgoing>Flow_1h3v8z9</bpmn:outgoing>
    </bpmn:startEvent>
    <bpmn:task id="Activity_0czh9p7" name="idea thinking">
      <bpmn:incoming>Flow_1h3v8z9</bpmn:incoming>
    </bpmn:task>
    <bpmn:sequenceFlow id="Flow_1h3v8z9" sourceRef="StartEvent_159a0qr" targetRef="Activity_0czh9p7" />
  </bpmn:process>
  <bpmn:process id="Process_0wcxzi5">
    <bpmn:task id="Activity_022ndt8" name="idea listing" />
    <bpmn:task id="Activity_13hbii9" name="update the status and link" />
  </bpmn:process>
  <bpmn:process id="Process_11gzt64">
    <bpmn:task id="Activity_1je3r2b" name="generate 5 caption based on idea" />
    <bpmn:task id="Activity_085ulwn" name="generate 5 prompt based on idea" />
  </bpmn:process>
  <bpmn:process id="Process_0m6ibzc">
    <bpmn:task id="Activity_1me3o3i" name="generate 5 img based on 5 prompt" />
  </bpmn:process>
  <bpmn:process id="Process_1auvgky">
    <bpmn:task id="Activity_16qhb17" name="5 img to 5 vid using same 5 prompt" />
  </bpmn:process>
  <bpmn:process id="Process_1yn7l45">
    <bpmn:task id="Activity_1yajq2o" name="generate 5 sound using 5 prompt" />
  </bpmn:process>
  <bpmn:process id="Process_0cah0cf">
    <bpmn:task id="Activity_0bl3gqg" name="edit to merge all">
      <bpmn:outgoing>Flow_1fgs2rl</bpmn:outgoing>
    </bpmn:task>
    <bpmn:task id="Activity_0rfaq6y" name="export final output">
      <bpmn:incoming>Flow_1fgs2rl</bpmn:incoming>
    </bpmn:task>
    <bpmn:sequenceFlow id="Flow_1fgs2rl" sourceRef="Activity_0bl3gqg" targetRef="Activity_0rfaq6y" />
  </bpmn:process>
  <bpmn:process id="Process_0irng22">
    <bpmn:task id="Activity_0tg4iy1" name="uploaded to google drive" />
  </bpmn:process>
  <bpmndi:BPMNDiagram id="BPMNDiagram_1">
    <bpmndi:BPMNPlane id="BPMNPlane_1" bpmnElement="Collaboration_0l6ul9b">
      <bpmndi:BPMNShape id="Participant_0p3g1rl_di" bpmnElement="Participant_0p3g1rl" isHorizontal="true">
        <dc:Bounds x="152" y="80" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="_BPMNShape_StartEvent_2" bpmnElement="StartEvent_159a0qr">
        <dc:Bounds x="202" y="162" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0czh9p7_di" bpmnElement="Activity_0czh9p7">
        <dc:Bounds x="290" y="140" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_1h3v8z9_di" bpmnElement="Flow_1h3v8z9">
        <di:waypoint x="238" y="180" />
        <di:waypoint x="290" y="180" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_1bna06k_di" bpmnElement="Participant_1bna06k" isHorizontal="true">
        <dc:Bounds x="152" y="410" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_022ndt8_di" bpmnElement="Activity_022ndt8">
        <dc:Bounds x="290" y="450" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_13hbii9_di" bpmnElement="Activity_13hbii9">
        <dc:Bounds x="620" y="470" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_0hubn45_di" bpmnElement="Participant_0hubn45" isHorizontal="true">
        <dc:Bounds x="152" y="660" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1je3r2b_di" bpmnElement="Activity_1je3r2b">
        <dc:Bounds x="530" y="710" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_085ulwn_di" bpmnElement="Activity_085ulwn">
        <dc:Bounds x="290" y="770" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_0xrni4t_di" bpmnElement="Participant_0xrni4t" isHorizontal="true">
        <dc:Bounds x="152" y="910" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1me3o3i_di" bpmnElement="Activity_1me3o3i">
        <dc:Bounds x="290" y="970" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_0qib768_di" bpmnElement="Participant_0qib768" isHorizontal="true">
        <dc:Bounds x="152" y="1160" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_16qhb17_di" bpmnElement="Activity_16qhb17">
        <dc:Bounds x="460" y="1230" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_1y5125u_di" bpmnElement="Participant_1y5125u" isHorizontal="true">
        <dc:Bounds x="910" y="910" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1yajq2o_di" bpmnElement="Activity_1yajq2o">
        <dc:Bounds x="1000" y="970" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_0ktswqz_di" bpmnElement="Participant_0ktswqz" isHorizontal="true">
        <dc:Bounds x="910" y="1160" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0bl3gqg_di" bpmnElement="Activity_0bl3gqg">
        <dc:Bounds x="1000" y="1240" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0rfaq6y_di" bpmnElement="Activity_0rfaq6y">
        <dc:Bounds x="1200" y="1240" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_1fgs2rl_di" bpmnElement="Flow_1fgs2rl">
        <di:waypoint x="1100" y="1280" />
        <di:waypoint x="1200" y="1280" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_1qnspw5_di" bpmnElement="Participant_1qnspw5" isHorizontal="true">
        <dc:Bounds x="910" y="410" width="600" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0tg4iy1_di" bpmnElement="Activity_0tg4iy1">
        <dc:Bounds x="1200" y="480" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_13txqb1_di" bpmnElement="Flow_13txqb1">
        <di:waypoint x="340" y="220" />
        <di:waypoint x="340" y="450" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1pfxenp_di" bpmnElement="Flow_1pfxenp">
        <di:waypoint x="340" y="530" />
        <di:waypoint x="340" y="770" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_11dwuw0_di" bpmnElement="Flow_11dwuw0">
        <di:waypoint x="390" y="490" />
        <di:waypoint x="590" y="490" />
        <di:waypoint x="590" y="710" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1koptz8_di" bpmnElement="Flow_1koptz8">
        <di:waypoint x="340" y="850" />
        <di:waypoint x="340" y="970" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0t182xq_di" bpmnElement="Flow_0t182xq">
        <di:waypoint x="340" y="1050" />
        <di:waypoint x="340" y="1270" />
        <di:waypoint x="460" y="1270" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0gp79au_di" bpmnElement="Flow_0gp79au">
        <di:waypoint x="390" y="830" />
        <di:waypoint x="500" y="830" />
        <di:waypoint x="500" y="1230" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1ftuigg_di" bpmnElement="Flow_1ftuigg">
        <di:waypoint x="390" y="810" />
        <di:waypoint x="1060" y="810" />
        <di:waypoint x="1060" y="970" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_15sgib1_di" bpmnElement="Flow_15sgib1">
        <di:waypoint x="560" y="1270" />
        <di:waypoint x="1000" y="1270" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1chlh2j_di" bpmnElement="Flow_1chlh2j">
        <di:waypoint x="1050" y="1050" />
        <di:waypoint x="1050" y="1240" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_09b9734_di" bpmnElement="Flow_09b9734">
        <di:waypoint x="580" y="790" />
        <di:waypoint x="580" y="1100" />
        <di:waypoint x="1020" y="1100" />
        <di:waypoint x="1020" y="1230" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0b9qu4h_di" bpmnElement="Flow_0b9qu4h">
        <di:waypoint x="1250" y="1240" />
        <di:waypoint x="1250" y="560" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1wmq128_di" bpmnElement="Flow_1wmq128">
        <di:waypoint x="1200" y="520" />
        <di:waypoint x="720" y="520" />
      </bpmndi:BPMNEdge>
    </bpmndi:BPMNPlane>
  </bpmndi:BPMNDiagram>
</bpmn:definitions>
