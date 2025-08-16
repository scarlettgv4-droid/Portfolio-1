import React from "react"; import { motion } from "framer-motion"; import { Github, Linkedin, Mail, Phone, MapPin, Link as LinkIcon, ExternalLink, ArrowRight, Terminal, Briefcase, GraduationCap, Image as ImageIcon, FileDown } from "lucide-react";

const PROFILE = { name: "Somia Mazzouzi", role: "Translator | Data Annotator | Language Specialist", tagline: "Multilingual translator and data annotator with expertise in AI training, linguistic quality assurance, and cultural adaptation.", availability: "Open to opportunities in translation, AI data annotation, and linguistic QA", location: "Tlemcen, Algeria", email: "Scarlettgv4@gmail.com", phone: "0657188307", socials: [ { label: "GitHub", href: "https://github.com/yourname", icon: Github }, { label: "LinkedIn", href: "https://www.linkedin.com/in/yourname", icon: Linkedin }, { label: "Email", href: "mailto:Scarlettgv4@gmail.com", icon: Mail }, { label: "Phone", href: "tel:0657188307", icon: Phone }, ], photo: "/profile.jpg", cv: "/Somia-Mazzouzi-CV.pdf", // place your resume PDF in public folder about: Detail-oriented translator and data annotator with over three years of experience in multilingual translation, data labeling, and AI training. Worked with Samsung Technologies, Xpeng Motors, and leading UAE institutions. Skilled in cultural nuance, CAT tools, and AI model training., focus: "Translation & Localization, Data Annotation, AI Voice Generation, Linguistic QA.", };

const SKILLS = { translation: ["English", "Arabic", "French", "Spanish"], annotation: ["Text", "Audio", "Image", "Video"], ai: ["AI Voice Generation", "Transcription", "TTS/STT Training"], tools: ["CAT Tools", "Data Labeling Platforms", "AI Training Software"], };

const PROJECTS = [ { title: "Samsung & Xpeng Data Annotation", blurb: "Labeled and reviewed multilingual datasets ensuring cultural accuracy and linguistic quality.", stack: ["French", "Arabic", "English", "Annotation"], links: [{ label: "Overview", href: "#" }], }, { title: "Legal & Financial Translation UAE", blurb: "Translated sensitive legal and financial documents for UAE authorities and top firms.", stack: ["Translation", "Localization", "Confidentiality"], links: [{ label: "Case Study", href: "#" }], }, { title: "AI Voice Generation (TTS QA)", blurb: "Generated voice datasets for Arabic, English, and French TTS systems and trained models for accuracy.", stack: ["AI", "Voice", "Multilingual"], links: [{ label: "Demo", href: "#" }], }, ];

const EXPERIENCE = [ { role: "French Data Annotator & Labeler", org: "Digital Gate & Summa Linguae", period: "Nov 2024 – Present", points: [ "Annotated and labeled French datasets for AI training.", "Collaborated with Samsung Technologies & Xpeng Motors.", "Ensured linguistic accuracy in AI datasets.", ], }, { role: "Translator & Language Specialist", org: "TransPro", period: "Dec 2021 – Present", points: [ "Translated and localized legal, financial, and technical documents for UAE clients.", "Clients include IATA Travel Centre UAE, Federal Authority for Identity & Citizenship UAE, and Index Exchange UAE.", "Maintained confidentiality and context accuracy.", ], }, { role: "AI Voice Generator & Language Model Trainer", org: "Freelance", period: "2023 – Present", points: [ "Generated AI voice samples for multilingual speech synthesis.", "Trained models for pronunciation and intonation accuracy.", "Enhanced TTS/STT technologies with linguistic expertise.", ], }, ];

const EDUCATION = [ { title: "M.A. in Language Sciences", org: "University Abu Bakr Belkaid", period: "2020 – 2022", }, { title: "B.A. in English Language & Literature", org: "University Abu Bakr Belkaid", period: "2017 – 2020", }, { title: "Baccalauréat in Foreign Languages", org: "Kharbouche Mohammed High School", period: "2012 – 2015", }, ];

const GALLERY = [ { src: "/gallery/certificate1.jpg", caption: "Certificate of Appreciation – Global Virtual Classroom 2019" }, { src: "/gallery/certificate2.jpg", caption: "Soroban Trainer Certification – Khacha Center 2020" }, { src: "/gallery/work1.jpg", caption: "Sample of multilingual translation work" }, ];

const Container = ({ id, className = "", children }) => (

  <section id={id} className={`max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 ${className}`}>
    {children}
  </section>
);const SectionTitle = ({ children }) => (

  <h2 className="text-2xl sm:text-3xl font-bold tracking-tight mb-6">{children}</h2>
);const Pill = ({ children }) => ( <span className="inline-flex items-center rounded-full border px-3 py-1 text-xs sm:text-sm"> {children} </span> );

const Card = ({ className = "", children }) => (

  <div className={`rounded-2xl border p-5 shadow-sm bg-white/60 backdrop-blur ${className}`}>{children}</div>
);export default function PortfolioTemplate() { return ( <div className="min-h-screen w-full bg-gradient-to-b from-slate-50 via-white to-slate-50 text-slate-900"> {/* Nav */} <header className="sticky top-0 z-30 backdrop-blur bg-white/70 border-b"> <Container className="flex items-center justify-between py-3"> <div className="font-extrabold tracking-tight text-lg">{PROFILE.name.split(" ")[0]}<span className="text-slate-500">.</span></div> <nav className="hidden md:flex gap-6 text-sm"> <a href="#about" className="hover:underline">About</a> <a href="#skills" className="hover:underline">Skills</a> <a href="#projects" className="hover:underline">Projects</a> <a href="#gallery" className="hover:underline">Gallery</a> <a href="#experience" className="hover:underline">Experience</a> <a href="#contact" className="hover:underline">Contact</a> </nav> <div className="hidden sm:flex gap-3"> <a href={PROFILE.cv} download className="inline-flex items-center gap-2 rounded-full border px-4 py-2 text-sm"> <FileDown size={16} /> <span>Download CV</span> </a> <a href="#contact" className="inline-flex items-center gap-2 rounded-full border px-4 py-2 text-sm"> <span>Contact</span> <ArrowRight size={16} /> </a> </div> </Container> </header>

{/* Hero and other sections (same as before) */}
  <Container className="py-16 sm:py-24">
    <div className="grid lg:grid-cols-2 gap-10 items-center">
      <div>
        <motion.p initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.4 }} className="mb-3 text-xs sm:text-sm">
          {PROFILE.availability}
        </motion.p>
        <motion.h1 initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ delay: 0.05, duration: 0.5 }} className="text-3xl sm:text-5xl font-extrabold tracking-tight">
          Hi, I'm {PROFILE.name.split(" ")[0]} <span className="text-slate-500">{PROFILE.name.split(" ")[1] ?? ""}</span>
        </motion.h1>
        <motion.p initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ delay: 0.1, duration: 0.5 }} className="mt-3 text-xl font-semibold">
          {PROFILE.role}
        </motion.p>
        <motion.p initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ delay: 0.15, duration: 0.5 }} className="mt-4 text-slate-700">
          {PROFILE.tagline}
        </motion.p>
        <div className="mt-6 flex flex-wrap items-center gap-3">
          <a href="#projects" className="inline-flex items-center gap-2 rounded-full border px-4 py-2 text-sm">
            <span>View My Work</span>
            <ExternalLink size={16} />
          </a>
          <a href={PROFILE.cv} download className="inline-flex items-center gap-2 rounded-full border px-4 py-2 text-sm">
            <FileDown size={16} /> <span>Download CV</span>
          </a>
        </div>
      </div>
      <Card className="lg:ml-auto lg:max-w-md text-center">
        <img src={PROFILE.photo} alt="Profile" className="w-40 h-40 mx-auto rounded-full object-cover border-4 border-slate-200 shadow-md" />
        <div className="mt-4 space-y-2">
          <div className="flex items-center justify-center gap-2 text-slate-700"><MapPin size={16} /> {PROFILE.location}</div>
          <div className="flex items-center justify-center gap-2 text-slate-700"><Mail size={16} /> {PROFILE.email}</div>
          <div className="flex items-center justify-center gap-2 text-slate-700"><Phone size={16} /> {PROFILE.phone}</div>
          <div className="flex flex-wrap gap-3 pt-2 justify-center">
            {PROFILE.socials.map((s, i) => (
              <a key={i} href={s.href} className="inline-flex items-center gap-2 rounded-full border px-3 py-1 text-sm">
                {React.createElement(s.icon, { size: 16 })}
                <span>{s.label}</span>
              </a>
            ))}
          </div>
        </div>
      </Card>
    </div>
  </Container>

  {/* Gallery */}
  <Container id="gallery" className="py-12">
    <SectionTitle>Portfolio Gallery</SectionTitle>
    <div className="grid sm:grid-cols-2 md:grid-cols-3 gap-6">
      {GALLERY.map((item, i) => (
        <Card key={i} className="overflow-hidden text-center">
          <img src={item.src} alt={item.caption} className="w-full h-48 object-cover rounded-lg" />
          <p className="mt-3 text-sm text-slate-700 flex items-center justify-center gap-2"><ImageIcon size={14}/> {item.caption}</p>
        </Card>
      ))}
    </div>
  </Container>

  {/* Other sections (About, Skills, Projects, Experience, Contact) remain same */}
</div>

); }

