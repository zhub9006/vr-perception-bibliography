# Annotated Bibliography: VR Perception Research
### Sensory Congruence, Depth Perception & Multisensory Integration in Virtual Environments

> **Maintained by:** VR Perception Research Group  
> **Last Updated:** June 2026  
> **Repository:** [zhub9006/vr-perception-bibliography](https://github.com/zhub9006/vr-perception-bibliography)

---

## How to Use This Bibliography

This document collects and annotates open-source GitHub repositories relevant to our research on **sensory congruence** and **depth perception in virtual reality**. Each entry includes:
- A full repository citation with URL
- A description of the project's scope and methods
- A **Relevance** note explaining how it connects to our group's work
- A **Limitations / Notes** section for critical context

Entries are organised into thematic sections. A notes section at the end documents the state of local `/data` literature files audited during compilation.

---

## Section 1 — Depth Perception Experiments in VR

---

### 1.1 `yisusgoenaga/depth-perception-vr`

**Citation:**  
Goenaga, Y. (n.d.). *depth-perception-vr: Aplicación Unity para Meta Quest 2 — Tareas de percepción de profundidad estereoscópica* [Unity/ShaderLab application]. GitHub. https://github.com/yisusgoenaga/depth-perception-vr

**Description:**  
A Unity application built for the Meta Quest 2 standalone headset, developed as part of a doctoral thesis in Cognitive Sciences at the Universidad Autónoma de Madrid (UAM). The repository implements stereoscopic depth-perception tasks — experimental paradigms in which participants make judgements about object distances and relative depths using binocular disparity cues delivered through the Quest 2's display. The project is structured with standard Unity directories (`Assets/`, `Packages/`, `ProjectSettings/`) alongside a `PrepareData/` folder suggesting automated data-pipeline tooling. Primary language is ShaderLab, indicating custom rendering shaders for precise stereoscopic control.

**Relevance to Research Group:**  
This repository is directly relevant to our **stereoscopic depth cue** work. The use of a standalone, inside-out tracked headset (Meta Quest 2) mirrors our own hardware setup, making the experimental paradigms potentially portable to our lab. The doctoral-thesis context (UAM Cognitive Sciences) situates the work firmly in cognitive/perceptual science rather than engineering, aligning with our theoretical framing. The `PrepareData/` pipeline is worth examining for data-preprocessing strategies applicable to our own depth-judgement tasks.

**Limitations / Notes:**  
No README is present, so experimental protocol details (stimulus parameters, trial structure, dependent variables) must be inferred from source code. No published companion paper has been identified at time of writing. Contact the author for thesis documentation.

---

### 1.2 `vrperceptionstudy/vrperceptionstudy.github.io`

**Citation:**  
Arora, R., Li, J., Shi, G., & Singh, K. (2020). *VR Depth and Size Perception Study* [Research study website]. Dynamic Graphics Project, University of Toronto. GitHub Pages. https://github.com/vrperceptionstudy/vrperceptionstudy.github.io

**Description:**  
The public-facing website for a crowdsourced perceptual study run by the Dynamic Graphics Project (DGP) lab at the University of Toronto. The study recruited participants who owned six-degrees-of-freedom (6DOF) VR devices (Oculus Rift, HTC Vive, Valve Index, Windows Mixed Reality, Oculus Quest) to complete a 15–20 minute computerised experiment assessing **size and depth perception accuracy** in virtual environments. Participants downloaded a lightweight application, completed up to three sessions for leaderboard ranking, and received detailed performance reports. The study ran until August 31, 2020. Investigators: Karan Singh (PI), Rahul Arora, Jiannan Li, and Gongyi Shi. The repository hosts a Jekyll/SCSS static site with a detailed `index.md` covering study protocol, compensation (US $5 gift card + leaderboard bonus), FAQ, and participant instructions.

**Relevance to Research Group:**  
This is one of the few examples of a **large-scale, crowdsourced VR perceptual study** with rigorous participant management. The multi-session design (up to 3 sessions, with bonus points) and the automated performance-report pipeline offer a methodological template for our own remote or semi-remote data collection efforts. The focus on both **size and depth perception** across multiple consumer headset types provides cross-device ecological validity data that is difficult to obtain in single-lab settings. The leaderboard gamification strategy is also worth noting as a participant-retention technique.

**Limitations / Notes:**  
The study concluded in 2020; the leaderboard server (Heroku) may be offline. No peer-reviewed publication has been confirmed linked to this repository at time of writing — follow up with the DGP lab (dgp.toronto.edu) for any resulting papers. Raw data is not publicly released through this repository.

---

### 1.3 `Lumbo1379/vr-dissertation`

**Citation:**  
Lumbo. (n.d.). *Can Virtual Reality be Used to Accurately Perceive Depth Perception?* [Undergraduate/postgraduate dissertation, PDF]. GitHub. https://github.com/Lumbo1379/vr-dissertation

**Description:**  
A single-document repository hosting a full dissertation PDF that directly addresses the central question of whether VR systems can support accurate depth perception. The dissertation presumably reviews the literature on depth cues (binocular disparity, motion parallax, vergence, accommodation) and evaluates empirical evidence for and against the fidelity of VR-mediated depth perception relative to real-world viewing. The repository has no README or supplementary materials beyond the PDF itself.

**Relevance to Research Group:**  
Serves as a useful **literature synthesis and framing document** for our group. The dissertation's central question — whether VR accurately mediates depth perception — is precisely the theoretical backdrop against which our own empirical work is situated. It can be used as an onboarding reading for new group members and as a source for tracing the empirical literature the author cites. Particularly useful for contextualising known limitations such as the vergence–accommodation conflict and the compression of egocentric distance in HMDs.

**Limitations / Notes:**  
Academic level and institutional affiliation are not stated in the repository metadata. The PDF has not been peer-reviewed. Treat as a secondary synthesis source rather than primary empirical evidence. The full reference list within the PDF should be mined for primary literature.

---

### 1.4 `StephenSoftwareDeveloper/3DdepthPerceptionInBlender`

**Citation:**  
Stephen Software Developer. (n.d.). *3DdepthPerceptionInBlender: Python script for stereoscopic camera rigs in Blender* [Python/Blender tool]. GitHub. https://github.com/StephenSoftwareDeveloper/3DdepthPerceptionInBlender

**Description:**  
A Python scripting tool for Blender that automates the creation of stereoscopic camera rigs simulating 3D depth perception. The script generates two cameras with a configurable inter-ocular offset — objects too close or too far from the viewer produce the binocular disparity pattern characteristic of natural stereo vision. The tool supports both still-image rendering and animation rendering, and is explicitly designed for VR, AR, and 3D monitor output. Two scripts are provided: `create_cameras` (rig generation) and `create_composites` (node-based compositing for the stereo pair). The project has 3 stars on GitHub.

**Relevance to Research Group:**  
Directly useful for our **stimulus generation pipeline**. When designing controlled depth-perception experiments, precise manipulation of binocular disparity is essential. This Blender tool offers a programmable, reproducible way to generate stereoscopic stimuli with exact inter-ocular distance and convergence parameters — parameters that map directly onto the theoretical variables in our sensory congruence models. The compositing workflow is also relevant for creating stimuli with controlled disparity gradients across a scene.

**Limitations / Notes:**  
No formal documentation of the disparity calculation model or validation against known perceptual thresholds. The tool should be validated against published stereo rendering standards (e.g., SMPTE ST 2096) before use in published experiments. No associated publication or institutional affiliation.

---

## Section 2 — Related Bibliography Repository

---

### 2.1 `zhub9006/vr-perception-bibliography` *(this repository)*

**Citation:**  
VR Perception Research Group. (2026). *vr-perception-bibliography: Annotated bibliography for VR perception research* [Markdown document]. GitHub. https://github.com/zhub9006/vr-perception-bibliography

**Description:**  
This living annotated bibliography — the document you are reading — is maintained by the VR Perception Research Group to consolidate open-source resources, experimental tools, and literature on sensory congruence, depth perception, visuomotor adaptation, and embodiment in virtual environments. It is updated as new repositories and notes are identified.

**Relevance to Research Group:**  
Central resource for onboarding, grant writing, and literature reviews. All group members are encouraged to contribute entries via pull request.

---

## Section 3 — Thematic Cross-Reference

The following table maps each repository to the core research themes of our group for quick reference:

| Repository | Depth Perception | Sensory Congruence | Stimulus Generation | Methods / Protocol | Theoretical Review |
|---|:---:|:---:|:---:|:---:|:---:|
| `yisusgoenaga/depth-perception-vr` | ✅ | ✅ | — | ✅ | — |
| `vrperceptionstudy/vrperceptionstudy.github.io` | ✅ | — | — | ✅ | — |
| `Lumbo1379/vr-dissertation` | ✅ | ✅ | — | — | ✅ |
| `StephenSoftwareDeveloper/3DdepthPerceptionInBlender` | ✅ | — | ✅ | — | — |

---

## Section 4 — Local `/data` Folder Audit

As part of compiling this bibliography, all files in the research group's local `/data` directory were audited for existing VR literature notes, annotation files, or reading summaries that could be incorporated.

**Audit Date:** June 2026  
**Directories Checked:** `/data/`, `/data/coursework/`, `/data/collections/`

**Outcome:** No VR-specific literature notes, annotation files, or reading summaries were found in the `/data` directory at time of compilation. The directory contains files related to medical research (MS treatment protocols, COVID-19 hospital data), music industry investment reports, finance summaries, and travel/event planning. The `coursework/Compiled_Research_Report.md` file contains an MS treatment protocol update and a COVID-19 hospital impact study — neither relevant to VR perception.

**Recommendation:** The group should establish a dedicated `/data/vr_literature/` subdirectory for storing future reading notes, annotation exports (e.g., from Zotero or Obsidian), and paper summaries. A suggested naming convention for annotation files is:

```
/data/vr_literature/
  AuthorYear_ShortTitle_notes.md       ← reading notes
  AuthorYear_ShortTitle_annot.md       ← formal annotation
  topic_depth_perception_overview.md   ← thematic syntheses
```

---

## Section 5 — Suggested Next Steps for the Research Group

1. **Add primary literature entries.** This bibliography currently covers only open-source software repositories. The group should add entries for key peer-reviewed papers (e.g., Cutting & Vishton 1995 on depth cues; Hibbard & Bradshaw 2003 on stereo depth; Witmer & Singer 1998 on presence; Ernst & Banks 2002 on multisensory integration).

2. **Link repositories to papers.** Where a GitHub repository has a companion publication (e.g., the Toronto VR perception study), retrieve the DOI and update the citation accordingly.

3. **Add tool repositories for VR frameworks.** Consider annotating OpenXR, Unity XR Toolkit, and WebXR repositories as infrastructure entries.

4. **Establish a contribution workflow.** Use GitHub Issues to propose new entries and Pull Requests to add them, with at least one group member reviewing each annotation before merge.

5. **Export to BibTeX.** For integration with LaTeX manuscripts, maintain a parallel `bibliography.bib` file with BibTeX entries for all citable items.

---

## Appendix — Search Queries Used

The following GitHub search queries were used to identify repositories for this bibliography:

| Query | Results |
|---|---|
| `sensory congruence virtual reality` | 0 repositories found |
| `depth perception VR` | 5 repositories found (4 relevant) |
| `sensory congruence multisensory VR perception` | 0 repositories found |
| `virtual reality embodiment visuomotor adaptation perception` | 0 repositories found |
| `stereoscopic depth cues VR experiment` | 0 repositories found |
| `vection presence immersion virtual reality perception experiment` | 0 repositories found |
| `audiovisual integration multisensory perception experiment` | 0 repositories found |

**Note on search coverage:** GitHub search indexes repository names, descriptions, and README content. Repositories with sparse or non-English metadata may not surface. Direct author outreach and forward/backward citation chaining from the dissertation (Entry 1.3) is recommended to supplement automated search.

---

*This document was compiled semi-automatically using GitHub repository search and local file audit tools. All annotations were written by the research assistant and should be reviewed by a domain expert before use in formal publications.*
