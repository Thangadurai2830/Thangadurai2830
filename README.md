import { useState } from "react";
import {
  Code2, Brain, Globe, Mail, Linkedin, Twitter, Instagram,
  Facebook, ExternalLink, Github, Star, GitFork, Layers,
  Database, Terminal, Cpu, FlaskConical, BarChart3, Zap,
  BookOpen, CheckCircle2, Circle, ChevronDown, ChevronUp,
  Shield, Cloud, Smartphone, ArrowUpRight, Sparkles,
  GraduationCap, Briefcase, MapPin, Activity
} from "lucide-react";

const GOLD = "#c9a84c";
const GOLD_DIM = "#8a6d2f";
const BG = "#0b0e14";
const SURFACE = "#111520";
const SURFACE2 = "#161b27";
const BORDER = "#1e2535";
const BORDER_GLOW = "#2a3450";
const TEXT = "#e8ecf4";
const MUTED = "#6b7799";
const ACCENT_BLUE = "#4a7fd4";
const ACCENT_TEAL = "#2dd4bf";

export default function GitHubProfile() {
  const [openSection, setOpenSection] = useState(null);
  const toggle = (s) => setOpenSection(openSection === s ? null : s);

  const skills = [
    {
      id: "frontend",
      icon: <Globe size={18} color={GOLD} />,
      label: "Frontend",
      items: ["React.js", "Tailwind CSS", "JavaScript", "TypeScript", "HTML5/CSS3", "GSAP", "Vite"],
    },
    {
      id: "backend",
      icon: <Terminal size={18} color={GOLD} />,
      label: "Backend",
      items: ["Node.js", "Express.js", "Spring Boot", "Django", "Flask", "Java", "Python"],
    },
    {
      id: "database",
      icon: <Database size={18} color={GOLD} />,
      label: "Database & Cloud",
      items: ["MongoDB", "MySQL", "Hibernate", "Netlify", "Vercel", "Render"],
    },
    {
      id: "ml",
      icon: <Brain size={18} color={GOLD} />,
      label: "AI / ML / Deep Learning",
      items: ["TensorFlow", "Keras", "PyTorch", "scikit-learn", "XGBoost", "Vision Transformer", "Swin Transformer", "SHAP", "LIME", "NLP", "Time Series"],
    },
    {
      id: "data",
      icon: <BarChart3 size={18} color={GOLD} />,
      label: "Data Science",
      items: ["Pandas", "NumPy", "Matplotlib", "Seaborn", "Plotly", "MLflow", "Google Colab"],
    },
    {
      id: "tools",
      icon: <Zap size={18} color={GOLD} />,
      label: "Dev Tools",
      items: ["Git", "GitHub", "Postman", "VS Code", "Docker (learning)"],
    },
  ];

  const projects = [
    {
      icon: <FlaskConical size={20} color={GOLD} />,
      title: "Diabetic Nephropathy Detection",
      subtitle: "Hybrid Deep & Machine Learning System",
      tags: ["TensorFlow", "React", "Django", "SHAP", "Vision Transformer"],
      desc: "Early detection of Diabetic Nephropathy fusing structured clinical data with retinal images. Ensemble of Vision Transformer + Swin Transformer with SHAP/LIME explainability for clinical-grade interpretability.",
      accent: GOLD,
    },
    {
      icon: <Layers size={20} color={ACCENT_TEAL} />,
      title: "E-Commerce Clothing Store",
      subtitle: "Full-featured MERN Stack Shop",
      tags: ["MongoDB", "Express", "React", "Node.js", "JWT"],
      desc: "End-to-end online store with product catalog, cart, JWT auth, role-based access, order tracking, admin dashboard, and payment gateway integration.",
      accent: ACCENT_TEAL,
    },
    {
      icon: <BookOpen size={20} color={ACCENT_BLUE} />,
      title: "Study Material Platform",
      subtitle: "Student–Teacher Collaboration Portal",
      tags: ["Node.js", "MongoDB", "React", "REST API"],
      desc: "Platform for uploading, organizing, and sharing academic resources with role-based dashboards for students and educators, plus engagement analytics.",
      accent: ACCENT_BLUE,
    },
    {
      icon: <Sparkles size={20} color="#a78bfa" />,
      title: "Gemini AI Clone",
      subtitle: "AI-Powered Conversational Assistant",
      tags: ["React", "Gemini API", "Tailwind CSS"],
      desc: "Real-time streaming chat assistant powered by Google Gemini API with persistent conversation history, animated UI, and session management.",
      accent: "#a78bfa",
    },
  ];

  const roadmap = [
    { done: true, label: "MERN Stack — production-grade architecture" },
    { done: true, label: "Transformer models — Vision & Language" },
    { done: true, label: "Model explainability — SHAP & LIME" },
    { done: false, label: "MLOps — CI/CD pipelines with MLflow & DVC" },
    { done: false, label: "Docker & Kubernetes — containerized deployments" },
    { done: false, label: "AWS / GCP — cloud ML infrastructure" },
    { done: false, label: "LLM fine-tuning — custom domain adaptation" },
    { done: false, label: "React Native — cross-platform mobile apps" },
  ];

  const socials = [
    { icon: <Linkedin size={16} />, label: "LinkedIn", href: "https://www.linkedin.com/in/thangadurai-g/" },
    { icon: <Github size={16} />, label: "GitHub", href: "https://github.com/Thangadurai2830" },
    { icon: <Globe size={16} />, label: "Portfolio", href: "https://thangadurai-freelancer-portfolio.netlify.app/" },
    { icon: <Mail size={16} />, label: "Email", href: "mailto:thangaduraibeit100@gmail.com" },
    { icon: <Twitter size={16} />, label: "X / Twitter", href: "https://x.com/Thanga_durai_30" },
    { icon: <Instagram size={16} />, label: "Instagram", href: "https://www.instagram.com/thanga_durai_2830/" },
    { icon: <Facebook size={16} />, label: "Facebook", href: "https://www.facebook.com/Silver.Screen.Spot" },
  ];

  const proficiency = [
    { label: "Full Stack Dev", pct: 90, color: GOLD },
    { label: "Machine Learning", pct: 85, color: ACCENT_TEAL },
    { label: "Deep Learning", pct: 75, color: ACCENT_BLUE },
    { label: "NLP", pct: 70, color: "#a78bfa" },
    { label: "Data Science", pct: 82, color: "#f472b6" },
    { label: "Cloud / DevOps", pct: 55, color: "#fb923c" },
  ];

  const s = {
    root: {
      background: BG,
      minHeight: "100vh",
      fontFamily: "'DM Sans', sans-serif",
      color: TEXT,
      padding: "0",
    },
    importFont: `
      @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap');
      * { box-sizing: border-box; margin: 0; padding: 0; }
      ::-webkit-scrollbar { width: 4px; }
      ::-webkit-scrollbar-track { background: ${BG}; }
      ::-webkit-scrollbar-thumb { background: ${GOLD_DIM}; border-radius: 2px; }
      @keyframes fadeUp {
        from { opacity: 0; transform: translateY(24px); }
        to { opacity: 1; transform: translateY(0); }
      }
      @keyframes shimmer {
        0% { background-position: -200% center; }
        100% { background-position: 200% center; }
      }
      @keyframes pulse-ring {
        0%, 100% { box-shadow: 0 0 0 0 rgba(201,168,76,0.15); }
        50% { box-shadow: 0 0 0 8px rgba(201,168,76,0); }
      }
      .fade-up { animation: fadeUp 0.6s ease both; }
      .skill-pill:hover { background: ${BORDER_GLOW} !important; color: ${GOLD} !important; border-color: ${GOLD_DIM} !important; transition: all 0.2s; }
      .project-card:hover { border-color: ${GOLD_DIM} !important; transform: translateY(-2px); transition: all 0.25s; }
      .social-btn:hover { background: ${SURFACE2} !important; border-color: ${GOLD_DIM} !important; color: ${GOLD} !important; }
      .stat-card:hover { border-color: ${GOLD_DIM} !important; }
      .roadmap-item:hover { background: ${SURFACE2} !important; }
      details summary { cursor: pointer; list-style: none; }
      details summary::-webkit-details-marker { display: none; }
    `,
  };

  return (
    <>
      <style>{s.importFont}</style>
      <div style={s.root}>

        {/* ── HERO ── */}
        <div style={{
          position: "relative",
          padding: "72px 40px 56px",
          borderBottom: `1px solid ${BORDER}`,
          overflow: "hidden",
        }}>
          {/* Grid decoration */}
          <div style={{
            position: "absolute", inset: 0, opacity: 0.04,
            backgroundImage: `linear-gradient(${BORDER} 1px, transparent 1px), linear-gradient(90deg, ${BORDER} 1px, transparent 1px)`,
            backgroundSize: "40px 40px",
          }} />
          {/* Gold accent line */}
          <div style={{
            position: "absolute", top: 0, left: 40, right: 40,
            height: "2px",
            background: `linear-gradient(90deg, transparent, ${GOLD}, transparent)`,
          }} />

          <div style={{ maxWidth: 900, margin: "0 auto", position: "relative" }}>
            {/* Badge row */}
            <div style={{ display: "flex", gap: 8, marginBottom: 28, flexWrap: "wrap" }}>
              {[
                { icon: <GraduationCap size={13} />, label: "B.Tech IT" },
                { icon: <Code2 size={13} />, label: "Full Stack Developer" },
                { icon: <Brain size={13} />, label: "AI / ML Engineer" },
                { icon: <Briefcase size={13} />, label: "Freelancer" },
                { icon: <MapPin size={13} />, label: "India" },
              ].map((b) => (
                <span key={b.label} style={{
                  display: "inline-flex", alignItems: "center", gap: 5,
                  background: SURFACE, border: `1px solid ${BORDER}`,
                  borderRadius: 20, padding: "4px 12px",
                  fontSize: 12, color: MUTED, fontWeight: 500, letterSpacing: "0.02em",
                }}>
                  <span style={{ color: GOLD }}>{b.icon}</span>
                  {b.label}
                </span>
              ))}
            </div>

            {/* Name */}
            <h1 style={{
              fontFamily: "'Cormorant Garamond', serif",
              fontSize: "clamp(44px, 7vw, 72px)",
              fontWeight: 700,
              lineHeight: 1.05,
              letterSpacing: "-0.02em",
              marginBottom: 18,
              color: TEXT,
            }}>
              Thangadurai{" "}
              <span style={{
                background: `linear-gradient(135deg, ${GOLD} 0%, #f0d080 50%, ${GOLD} 100%)`,
                backgroundSize: "200% auto",
                WebkitBackgroundClip: "text",
                WebkitTextFillColor: "transparent",
                animation: "shimmer 3s linear infinite",
              }}>G.</span>
            </h1>

            <p style={{
              fontSize: 17, color: MUTED, lineHeight: 1.7,
              maxWidth: 580, marginBottom: 36, fontWeight: 300,
            }}>
              Building intelligent web applications at the intersection of
              modern frontend, scalable backend, and production-grade ML systems.
              Passionate about turning complex data into clear decisions.
            </p>

            {/* CTA row */}
            <div style={{ display: "flex", gap: 12, flexWrap: "wrap" }}>
              <a href="https://thangadurai-freelancer-portfolio.netlify.app/" target="_blank" rel="noreferrer"
                style={{
                  display: "inline-flex", alignItems: "center", gap: 8,
                  background: GOLD, color: "#0b0e14", borderRadius: 8,
                  padding: "10px 22px", fontWeight: 600, fontSize: 14,
                  textDecoration: "none", letterSpacing: "0.02em",
                  animation: "pulse-ring 2.5s ease infinite",
                }}>
                <Globe size={15} /> View Portfolio <ArrowUpRight size={14} />
              </a>
              <a href="mailto:thangaduraibeit100@gmail.com"
                style={{
                  display: "inline-flex", alignItems: "center", gap: 8,
                  background: "transparent", color: TEXT,
                  border: `1px solid ${BORDER_GLOW}`, borderRadius: 8,
                  padding: "10px 22px", fontWeight: 500, fontSize: 14,
                  textDecoration: "none", letterSpacing: "0.02em",
                }}>
                <Mail size={15} /> Get In Touch
              </a>
            </div>
          </div>
        </div>

        <div style={{ maxWidth: 900, margin: "0 auto", padding: "48px 40px" }}>

          {/* ── IDENTITY CARD ── */}
          <div style={{
            background: SURFACE, border: `1px solid ${BORDER}`, borderRadius: 14,
            padding: "28px 32px", marginBottom: 40,
            borderLeft: `3px solid ${GOLD}`,
            fontFamily: "'DM Mono', monospace",
          }} className="fade-up">
            <div style={{ color: GOLD_DIM, fontSize: 13, marginBottom: 8 }}>identity.py</div>
            <pre style={{
              fontSize: 13, lineHeight: 2, overflowX: "auto",
              color: "#8899cc",
              whiteSpace: "pre-wrap",
            }}>{`class Thangadurai:
    name        = `}<span style={{ color: ACCENT_TEAL }}>"Thangadurai G"</span>{`
    role        = `}<span style={{ color: ACCENT_TEAL }}>["Full Stack Dev", "AI/ML Engineer", "Freelancer"]</span>{`
    education   = `}<span style={{ color: ACCENT_TEAL }}>"B.Tech Information Technology"</span>{`
    location    = `}<span style={{ color: ACCENT_TEAL }}>"India"</span>{`
    philosophy  = `}<span style={{ color: GOLD }}>"Build → Break → Learn → Repeat"</span></pre>
          </div>

          {/* ── SKILL STACK ── */}
          <SectionHeading icon={<Cpu size={18} color={GOLD} />} title="Tech Stack" />
          <div style={{ display: "flex", flexDirection: "column", gap: 4, marginBottom: 40 }}>
            {skills.map((sk) => {
              const isOpen = openSection === sk.id;
              return (
                <div key={sk.id} style={{
                  background: SURFACE, border: `1px solid ${isOpen ? BORDER_GLOW : BORDER}`,
                  borderRadius: 10, overflow: "hidden",
                  transition: "border-color 0.2s",
                }}>
                  <button
                    onClick={() => toggle(sk.id)}
                    style={{
                      width: "100%", display: "flex", alignItems: "center",
                      justifyContent: "space-between", gap: 12,
                      padding: "14px 20px", background: "transparent",
                      border: "none", cursor: "pointer", color: TEXT,
                    }}>
                    <span style={{ display: "flex", alignItems: "center", gap: 10 }}>
                      {sk.icon}
                      <span style={{ fontSize: 14, fontWeight: 500 }}>{sk.label}</span>
                    </span>
                    {isOpen
                      ? <ChevronUp size={15} color={MUTED} />
                      : <ChevronDown size={15} color={MUTED} />}
                  </button>
                  {isOpen && (
                    <div style={{
                      padding: "4px 20px 18px",
                      display: "flex", flexWrap: "wrap", gap: 8,
                    }}>
                      {sk.items.map((item) => (
                        <span key={item} className="skill-pill" style={{
                          background: BG, border: `1px solid ${BORDER}`,
                          borderRadius: 6, padding: "5px 12px",
                          fontSize: 12, color: MUTED, fontFamily: "'DM Mono', monospace",
                          cursor: "default", transition: "all 0.2s",
                        }}>{item}</span>
                      ))}
                    </div>
                  )}
                </div>
              );
            })}
          </div>

          {/* ── PROJECTS ── */}
          <SectionHeading icon={<Layers size={18} color={GOLD} />} title="Featured Projects" />
          <div style={{
            display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(380px, 1fr))",
            gap: 16, marginBottom: 48,
          }}>
            {projects.map((p) => (
              <div key={p.title} className="project-card" style={{
                background: SURFACE, border: `1px solid ${BORDER}`,
                borderRadius: 12, padding: "24px",
                borderTop: `2px solid ${p.accent}`,
                transition: "all 0.25s",
              }}>
                <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 10 }}>
                  <div style={{
                    width: 38, height: 38, borderRadius: 10,
                    background: `${p.accent}14`,
                    display: "flex", alignItems: "center", justifyContent: "center",
                  }}>
                    {p.icon}
                  </div>
                  <div>
                    <div style={{ fontSize: 15, fontWeight: 600, color: TEXT }}>{p.title}</div>
                    <div style={{ fontSize: 12, color: MUTED }}>{p.subtitle}</div>
                  </div>
                </div>
                <p style={{ fontSize: 13, color: MUTED, lineHeight: 1.7, marginBottom: 14 }}>{p.desc}</p>
                <div style={{ display: "flex", flexWrap: "wrap", gap: 6 }}>
                  {p.tags.map((t) => (
                    <span key={t} style={{
                      background: BG, border: `1px solid ${BORDER}`,
                      borderRadius: 4, padding: "3px 9px",
                      fontSize: 11, color: MUTED, fontFamily: "'DM Mono', monospace",
                    }}>{t}</span>
                  ))}
                </div>
              </div>
            ))}
          </div>

          {/* ── PROFICIENCY ── */}
          <SectionHeading icon={<Activity size={18} color={GOLD} />} title="Skill Proficiency" />
          <div style={{
            background: SURFACE, border: `1px solid ${BORDER}`,
            borderRadius: 12, padding: "28px 32px", marginBottom: 48,
          }}>
            {proficiency.map((p, i) => (
              <div key={p.label} style={{ marginBottom: i < proficiency.length - 1 ? 18 : 0 }}>
                <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 6 }}>
                  <span style={{ fontSize: 13, color: TEXT, fontWeight: 500 }}>{p.label}</span>
                  <span style={{ fontSize: 13, color: MUTED, fontFamily: "'DM Mono', monospace" }}>{p.pct}%</span>
                </div>
                <div style={{ height: 4, background: BORDER, borderRadius: 4 }}>
                  <div style={{
                    height: "100%", width: `${p.pct}%`,
                    background: p.color, borderRadius: 4,
                    transition: "width 1s ease",
                  }} />
                </div>
              </div>
            ))}
          </div>

          {/* ── ROADMAP ── */}
          <SectionHeading icon={<Star size={18} color={GOLD} />} title="2025 Learning Roadmap" />
          <div style={{
            background: SURFACE, border: `1px solid ${BORDER}`,
            borderRadius: 12, padding: "8px 0", marginBottom: 48,
          }}>
            {roadmap.map((r, i) => (
              <div key={i} className="roadmap-item" style={{
                display: "flex", alignItems: "center", gap: 14,
                padding: "13px 24px",
                borderBottom: i < roadmap.length - 1 ? `1px solid ${BORDER}` : "none",
                transition: "background 0.2s",
              }}>
                {r.done
                  ? <CheckCircle2 size={16} color={ACCENT_TEAL} />
                  : <Circle size={16} color={BORDER_GLOW} />}
                <span style={{ fontSize: 14, color: r.done ? TEXT : MUTED, lineHeight: 1.5 }}>
                  {r.label}
                </span>
                {r.done && (
                  <span style={{
                    marginLeft: "auto", fontSize: 11, color: ACCENT_TEAL,
                    background: `${ACCENT_TEAL}14`, border: `1px solid ${ACCENT_TEAL}30`,
                    borderRadius: 4, padding: "2px 8px", fontWeight: 500,
                  }}>done</span>
                )}
              </div>
            ))}
          </div>

          {/* ── GITHUB STATS ── */}
          <SectionHeading icon={<Github size={18} color={GOLD} />} title="GitHub Analytics" />
          <div style={{
            display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(260px, 1fr))",
            gap: 12, marginBottom: 48,
          }}>
            {[
              { src: "https://github-readme-stats.vercel.app/api?username=Thangadurai2830&theme=transparent&hide_border=true&show_icons=true&title_color=c9a84c&icon_color=c9a84c&text_color=8899cc&bg_color=00000000", alt: "stats" },
              { src: "https://github-readme-stats.vercel.app/api/top-langs/?username=Thangadurai2830&theme=transparent&hide_border=true&layout=compact&title_color=c9a84c&text_color=8899cc&bg_color=00000000", alt: "langs" },
            ].map((img) => (
              <div key={img.alt} className="stat-card" style={{
                background: SURFACE, border: `1px solid ${BORDER}`,
                borderRadius: 12, padding: "20px",
                display: "flex", alignItems: "center", justifyContent: "center",
                overflow: "hidden", transition: "border-color 0.2s",
              }}>
                <img src={img.src} alt={img.alt} style={{ width: "100%", maxWidth: 360 }} />
              </div>
            ))}
          </div>
          <div style={{
            background: SURFACE, border: `1px solid ${BORDER}`,
            borderRadius: 12, padding: "20px", marginBottom: 48,
            display: "flex", alignItems: "center", justifyContent: "center",
          }}>
            <img
              src="https://nirzak-streak-stats.vercel.app/?user=Thangadurai2830&theme=transparent&hide_border=true&ring=c9a84c&fire=c9a84c&currStreakLabel=c9a84c&sideLabels=8899cc&currStreakNum=e8ecf4&sideNums=e8ecf4&dates=6b7799&background=00000000"
              alt="streak" style={{ width: "100%", maxWidth: 560 }}
            />
          </div>

          {/* ── SOCIALS ── */}
          <SectionHeading icon={<Mail size={18} color={GOLD} />} title="Connect With Me" />
          <div style={{ display: "flex", flexWrap: "wrap", gap: 10, marginBottom: 56 }}>
            {socials.map((sc) => (
              <a key={sc.label} href={sc.href} target="_blank" rel="noreferrer"
                className="social-btn"
                style={{
                  display: "inline-flex", alignItems: "center", gap: 8,
                  background: SURFACE, border: `1px solid ${BORDER}`,
                  borderRadius: 8, padding: "9px 16px",
                  fontSize: 13, color: TEXT, textDecoration: "none",
                  fontWeight: 500, transition: "all 0.2s",
                }}>
                <span style={{ color: GOLD }}>{sc.icon}</span>
                {sc.label}
                <ExternalLink size={12} color={MUTED} />
              </a>
            ))}
          </div>

          {/* ── FOOTER ── */}
          <div style={{
            borderTop: `1px solid ${BORDER}`,
            paddingTop: 32,
            display: "flex", flexDirection: "column", alignItems: "center", gap: 12, textAlign: "center",
          }}>
            <div style={{
              width: 40, height: 2, background: `linear-gradient(90deg, transparent, ${GOLD}, transparent)`,
              marginBottom: 8,
            }} />
            <p style={{
              fontFamily: "'Cormorant Garamond', serif",
              fontSize: 20, color: MUTED, fontStyle: "italic",
            }}>
              "Code is not just syntax — it's the art of solving real human problems."
            </p>
            <p style={{ fontSize: 12, color: `${MUTED}88` }}>
              Thangadurai G · Full Stack Developer & AI/ML Engineer · India
            </p>
          </div>

        </div>
      </div>
    </>
  );
}

function SectionHeading({ icon, title }) {
  return (
    <div style={{
      display: "flex", alignItems: "center", gap: 10,
      marginBottom: 20,
    }}>
      <div style={{
        width: 34, height: 34, borderRadius: 8,
        background: `rgba(201,168,76,0.1)`,
        border: `1px solid rgba(201,168,76,0.2)`,
        display: "flex", alignItems: "center", justifyContent: "center",
      }}>
        {icon}
      </div>
      <h2 style={{
        fontFamily: "'Cormorant Garamond', serif",
        fontSize: 22, fontWeight: 600,
        color: "#e8ecf4", letterSpacing: "0.01em",
      }}>{title}</h2>
      <div style={{
        flex: 1, height: "1px",
        background: `linear-gradient(90deg, rgba(201,168,76,0.3), transparent)`,
      }} />
    </div>
  );
}
