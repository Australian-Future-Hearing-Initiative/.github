# Australian Future Hearing Initiative (AFHI)

The **AFHI** is a collaborative research initiative bringing together [**Google Research**](https://blog.google/intl/en-au/company-news/technology/ai-hearing-initiative/) and world-leading organisations in hearing healthcare and accessibility associated with the [**Australian Hearing Hub**](https://hearinghub.edu.au/) at [**Macquarie University**](https://www.mq.edu.au/), [**Cochlear**](https://www.cochlear.com/), [**NextSense**](https://www.nextsense.org.au/), and [**The Shepherd Centre**](https://shepherdcentre.org.au/).

While modern hearing devices perform well in quiet rooms, they often struggle to support listeners in complex, noisy social environments. With over 1.5 billion people affected by hearing loss globally, AFHI applies machine learning (ML), biophysical computational modelling of the inner ear, wearable multi-sensor platforms, and accessible audiological testing to develop highly personalised hearing assistance.

## 🔗 Quick Links

* 🌐 **Official Website:** [australianfuturehearing.org](https://australianfuturehearing.org/) 
* 🎥 **Background Talk:** [The Future of Hearing – Simon Carlile (TEDxSydney)](https://www.youtube.com/watch?v=Vup_coDYOoo)
* 📰 **Collaboration Announcement:** [Google Australia Blog – AI Hearing Initiative](https://blog.google/intl/en-au/company-news/technology/ai-hearing-initiative/)
* 🎧 **Online Hearing Tests (Live App):** [afhi-hearing-tests.streamlit.app](https://afhi-hearing-tests.streamlit.app/)
* 📖 **PRISM Platform Documentation:** [australian-future-hearing-initiative.github.io/prism-docs](https://australian-future-hearing-initiative.github.io/prism-docs/)


## 🔓 Public Repositories

The following repositories are publicly accessible and open-source:

| Repository | Description | Links & Resources |
| :--- | :--- | :--- |
| [**`afhi-hearing-tests-public`**](https://github.com/Australian-Future-Hearing-Initiative/afhi-hearing-tests-public) | Web-based suite of audiometric and suprathreshold hearing tests built with Streamlit (Pure-Tone Audiometry, Pip PTA, Consonant Confusion / VCV, Categorical Loudness Scaling, and Tone Generator). | [Live Streamlit App](https://afhi-hearing-tests.streamlit.app/) |
| [**`prism-docs`**](https://github.com/Australian-Future-Hearing-Initiative/prism-docs) | Quarto documentation site for the PRISM ecosystem, including Researcher, Participant, and Developer setup guides. | [Documentation Site](https://australian-future-hearing-initiative.github.io/prism-docs/) |
| [**`prism-ml`**](https://github.com/Australian-Future-Hearing-Initiative/prism-ml) | Machine learning models, dataset build scripts, and training pipelines for hearing-device scene recognition: **AuditoryHuM** (auditory scene clustering), **AHEAD-DS** (hearing aid scenes dataset), and **OpenYAMNet / YAMNet+**. | [AHEAD-DS Paper](https://arxiv.org/abs/2508.10360) · [AuditoryHuM Paper](https://arxiv.org/abs/2602.19409) · [Hugging Face](https://huggingface.co/hzhongresearch) |
| [**`carfac-ephys`**](https://github.com/Australian-Future-Hearing-Initiative/carfac-ephys) | *In silico* reproduction of animal cochlear impairment electrophysiology (ABR Wave-I / CAP and EFR growth curves across synaptopathy and outer hair cell loss) using the CARFAC model. | Built on [google/carfac](https://github.com/google/carfac) |
| [**`jax-haspi-hasqi`**](https://github.com/Australian-Future-Hearing-Initiative/jax-haspi-hasqi) | Fast, lightweight JAX implementation of the **HASPI v2** (intelligibility) and **HASQI v2** (quality) hearing-aid perceptual metrics and NAL-R prescription rule, numerically faithful to `pyclarity==0.9.0`. | 4.2× faster steady-state evaluation without PyTorch/CUDA dependencies |
| [**`afhi-conventions`**](https://github.com/Australian-Future-Hearing-Initiative/afhi-conventions) | Organisation-wide engineering, testing, documentation, and participant data-privacy conventions (`AGENTS.md`) for human contributors and AI coding agents. | House rules for all AFHI codebases |

## 🔒 Collaborator & Internal Repositories

> [!NOTE]
> The repositories below are currently **Private** or **Internal** to AFHI organisation members and research partners (several are undergoing clinical and engineering validation prior to open-source release). If you are not logged into an authorised AFHI GitHub account, links to these repositories will return a `404` page.

### Hyper-Personalisation: Cochlear Modelling & Hearing Aid Processing

| Repository | Visibility | Description |
| :--- | :---: | :--- |
| [**`hp-acoustic`**](https://github.com/Australian-Future-Hearing-Initiative/hp-acoustic) | `Private` | Core JAX acoustic hearing model and training framework. Trains speech-enhancement models in the cochlear domain using differentiable healthy and impaired CARFAC and Gammatone models; defines the shared `AudioModel` protocol. |
| TODO | | |


## 📚 Selected Publications & Datasets

* **AuditoryHuM (2026):** *Auditory Scene Label Discovery and Clustering.* [arXiv:2602.19409](https://arxiv.org/abs/2602.19409) · [Dataset](https://huggingface.co/datasets/hzhongresearch/auditoryhum_supplementary) · [Interactive Demo](https://huggingface.co/spaces/hzhongresearch/auditoryhum_samples)
* **Conversational Difficulty Moments (2026):** Collins, J., Buzea, A., Collier, C., Rosen, A. B., Maclaren, J., Lyon, R. F., Miles, K., & Carlile, S. *Identifying hearing difficulty moments in conversational audio.* Trends in Hearing, 30. [doi:10.1177/23312165261446379](https://doi.org/10.1177/23312165261446379)
* **Multi-Sensor Communication Lab (2026):** Ibrahim, R. K., Miles, K., Maggs, L., Luthy, B., Kan, A., Richardson, M. J., Maclaren, J., Carlile, S., Smith, Z. M., & Buchholz, J. M. *Building a multi-sensor lab for interactive communication research: Challenges, workarounds, and lessons learned.* Trends in Hearing, 30. [doi:10.1177/23312165261470622](https://doi.org/10.1177/23312165261470622)
* **AHEAD-DS & OpenYAMNet / YAMNet+ (2025):** Zhong, H., Buchholz, J. M., Maclaren, J., Carlile, S., & Lyon, R. F. *A dataset and model for recognition of audiologically relevant environments for hearing aids: AHEAD-DS and YAMNet+.* [arXiv:2508.10360](https://arxiv.org/abs/2508.10360) · [AHEAD-DS Dataset](https://huggingface.co/datasets/hzhongresearch/ahead_ds) · [Models](https://huggingface.co/hzhongresearch/yamnetp_ahead_ds)
* **CARFAC v2 in MATLAB, NumPy, and JAX (2024):** Lyon, R. F., Schonberger, R., Slaney, M., Velimirović, M., & Yu, H. *The CARFAC v2 cochlear model in Matlab, NumPy, and JAX.* [arXiv:2404.17490](https://arxiv.org/abs/2404.17490) · [google/carfac](https://github.com/google/carfac)

For a full list of conference abstracts, presentations, and articles, visit the [AFHI Research & Publications page](https://australianfuturehearing.org/research/).

## 🤝 Contributing & Engineering Conventions

We welcome contributions to our tools, models, and demos. All contributors (human developers and coding agents) should follow our organisation-wide standards in [**`afhi-conventions`**](https://github.com/Australian-Future-Hearing-Initiative/afhi-conventions):

* **Focused Pull Requests:** Keep PRs small and scoped to a single concern, using Conventional Commit titles (`feat`, `fix`, `refactor`, `test`, `docs`, `ci`, `chore`, `perf`).
* **Verification:** Run the repository's configured formatters, linters, type checks, and test suites (typically managed via [`uv`](https://docs.astral.sh/uv/) for Python or `fvm` / `flutter test` for Flutter) before opening a PR.
* **Participant Data & Security:** Never commit participant-level data, audiograms, recordings, `.env` files, or credentials (`serviceAccountKey.json`, keystores) to any repository, issue, or PR.

## 📢 Contact

This organisation is maintained by the AFHI team. For questions, research inquiries, or collaboration opportunities:

* **Website & Study Participation:** [australianfuturehearing.org](https://australianfuturehearing.org/involved/)
* **Simon Carlile:** [scarille@google.com](mailto:scarille@google.com)
* **Julian Maclaren:** [jmaclaren@google.com](mailto:jmaclaren@google.com)

## 📄 License

Repositories in this organisation are typically licensed under the **MIT License**, **Apache 2.0**, or **CC-BY-NC** depending on the component. Please refer to the `LICENSE` or `LICENCE` file in each individual repository for specific terms.

