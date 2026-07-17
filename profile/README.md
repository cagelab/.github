# ✨ Welcome to CageLab ✨

## About CageLab

CageLab is a collaborative project to build a high-throughput and large-scale cognitive training and testing platform for many subjects. Home cage testing and training is a strong 3Rs refinement for cognitive neuroscience research. The problem with existing cognitive testing / training kiosks is they do not scale well as the subject count increases. We solve this by implementing a robust remote control interface for one-to-many or many-to-many communication between control and experiment systems; using asymmetric staircase to adaptively train subjects, and architecting a data pipeline using a neuroscience database ([Alyx, from IBL](https://github.com/cortex-lab/alyx)) and task metadata specifications ([HED Tags](https://www.hedtags.org), BIDs / EEGLab origin).

## 🚀 The components

- **Hardware** - design a low-cost and flexible to adjust cage-attached box, along with reward and input devices. Low-cost is important because as the number of devices increases, price-per-device becomes an issue. Using Aluminium T-slot allows flexible adaptation to different housing configurations compared to perspex or stainless steel enclosures.
- **Communication Middleware (cogmoteGO)** - a fast and flexible way to distribute neuroscience experiments and collect data from many devices. It uses a HTTP API across devices and talks via local ØMQ messaging to experimental code for robust many-to-many control.
- **Software (CageLab-Code)** - PsychToolbox-based task manager, enabling existing experiment code designed for the lab to work more quickly in the home environment. PTB, with the largest support of different device hardware and best-in-class timing remains the gold-standard way to run neuroscience tasks.
- **Data pipeline** - integrating [Alyx (International Brain Lab, ONE protocol pipeline)](https://docs.internationalbrainlab.org) for metadata, S3 servers for file storage, and [HED tags](https://hedtags.org) for event labelling, to efficiently scale data collection and data analysis to a large number of home environment test devices.
- **Task Design** - Unified design across different tasks. Automated cognitive training using a tuned asymmetric staircase: more standardised and adaptive training per subject, hopefully resulting is faster training times.
- **AI Automation** - CogmoteGO and Alyx offer REST APIs, and because our data is labeled with schema-backed event labels: agents can therefore be trained to understand AND use the tooling to parse data, observe devices, and update parameters, reducing the tedious parts of managing many subjects and refining tasks over time.

## 🌟 The Projects

Browse our [repositories](https://github.com/orgs/cagelab/repositories) to see what we're working on.

---

*Made with ❤️ by the CageLab team*
