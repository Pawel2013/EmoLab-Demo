# EmoLab System Overview

## 1. Purpose

EmoLab is an interactive research environment for synchronized inspection, replay, and interpretation of multimodal affect-related telemetry.

The system addresses a recurring problem in affective computing: outputs from speech, language, prosody, vocal events, speakers, faces, and interaction analysis are often distributed across different services, files, temporal resolutions, identifiers, and visualizations.

EmoLab provides a common session model in which these outputs can be preserved, aligned, replayed, compared, and interpreted together.

---

## 2. Design Principles

### Temporal coherence

Outputs generated at different levels of temporal granularity are mapped to a shared session timeline.

### Multimodal inspectability

Model outputs remain connected to source audio or video, transcript content, speaker structure, facial observations, and model-specific windows.

### Deterministic replay

A previously analysed session can be reloaded and revisited without repeating the full original inference process.

### Provenance preservation

Displayed results retain enough timing, modality, source, and model context to support later inspection and audit.

### Separation of prediction and interpretation

Model outputs are presented as computational predictions. Higher-level interpretations are explicitly represented as hypotheses for human review.

### Responsive modularity

The interface uses independently expandable cards so that complex sessions can be inspected progressively on desktop and mobile devices.

---

## 3. Session Model

A persistent EmoLab session may include:

- source audio and video;
- transcript words and utterances;
- word-level timestamps;
- speaker diarization and speaker runs;
- linguistic affect-related predictions;
- sentiment and toxicity layers;
- prosodic predictions;
- vocal-event predictions;
- facial detections, descriptions, Action Units, tracks, and crops;
- model-specific temporal windows;
- multimodal timelines;
- graph-based linguistic views;
- emotion trajectory maps;
- visualization metadata;
- generated reports;
- processing and provenance metadata.

Not every session must contain every modality.

---

## 4. Shared Temporal Representation

Different components may use different clocks and temporal conventions, including media playback time, recording time, word boundaries, speaker-turn intervals, frame timestamps, model-specific windows, event-arrival timestamps, and processing timestamps.

EmoLab maps available events to a common session timeline that coordinates media playback, transcript highlighting, speaker indicators, facial observations, timelines, trajectory maps, graph views, and replay cursors.

---

## 5. Synchronized Replay

During replay, multiple linked views are updated from a common temporal position:

- source audio or video;
- transcript words;
- speaker turns;
- linguistic predictions;
- prosodic predictions;
- vocal events;
- facial observations;
- area timelines;
- trajectory maps;
- EmoiTextGraph;
- cursor-based inspection components.

Users can play, pause, seek, revisit turning points, compare modalities, and move between high-level summaries and source-level evidence.

---

## 6. Responsive Card-Based Interface

EmoLab uses a vertically structured, responsive card interface designed for desktop, laptop, and mobile inspection workflows.

Cards can be expanded, collapsed, opened in full-screen mode, and combined into task-specific sequences. The vertical structure is therefore an intentional interaction model rather than a limitation.

---

## 7. Analytical Views

The current prototype includes synchronized playback, face timelines, speaker-diarized transcripts, waveform views, Emotion Pulses, EmoiTextGraph, multimodal area timelines, global timeline navigation, modality-specific emotion trajectory maps, Top-5 summaries, emotion sparklines, session-management controls, and affective-cognitive reports.

See the [System Gallery](system-gallery.md).

---

## 8. Persistent Session Bundles

Session bundles preserve timing, transcript, speaker, model-output, facial, visualization, and reporting information.

Benefits include reproducible replay, later qualitative inspection, independence from repeated external inference, preservation of historical model outputs, reliable conference demonstration, and audit of model behaviour and interpretation.

Persistence preserves what models produced. It does not validate those outputs as ground truth.

---

## 9. Affective-Cognitive Interpretation

The affective-cognitive agent transforms selected synchronized telemetry into a structured report containing affective background, phase models, turning points, leading indicators, cross-channel conflicts, working hypotheses, confidence levels, unknowns, and temporal-grounding audits.

The agent is designed to distinguish direct evidence from inference. Its output supports critical human interpretation rather than automated psychological judgment.

See [Affective-Cognitive Agent](affective-cognitive-agent.md).

---

## 10. Demonstration Scenario

A typical demonstration proceeds as follows:

1. open a prepared session;
2. play the source interaction;
3. introduce transcript and speaker structure;
4. navigate to a selected moment;
5. compare linguistic, prosodic, vocal, and facial outputs;
6. inspect agreement, disagreement, uncertainty, and provenance;
7. replay from a selected timestamp;
8. show a trajectory, graph, or timeline view;
9. present an affective-cognitive interpretation;
10. review hypotheses and unknowns.

---

## 11. Reliability Model

The conference demonstration uses a local application build, local media, a local session bundle, preserved telemetry, deterministic replay, and a prerecorded fallback video.

The core scenario does not require conference Wi-Fi.

---

## 12. Status

EmoLab is an active research prototype. The public repository contains documentation and demonstration materials. Source code is not publicly released.
