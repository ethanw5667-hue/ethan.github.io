import { useState } from "react";
import { motion } from "framer-motion";
import { Menu, X, Download, Mail, Github, Linkedin, FileText, Briefcase, GraduationCap, Sparkles } from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";

export default function PortfolioSite() {
  const [open, setOpen] = useState(false);

  const navItems = [
    { label: "Home", href: "#home" },
    { label: "About", href: "#about" },
    { label: "Projects", href: "#projects" },
    { label: "Resume & CV", href: "#resume" },
    { label: "Contact", href: "#contact" },
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-slate-950 via-slate-900 to-slate-950 text-slate-100">
      {/* Nav */}
      <header className="sticky top-0 z-50 backdrop-blur supports-[backdrop-filter]:bg-slate-950/60 border-b border-slate-800">
        <div className="mx-auto max-w-6xl px-4">
          <div className="flex h-16 items-center justify-between">
            <a href="#home" className="flex items-center gap-2 font-semibold tracking-tight">
              <Sparkles className="h-5 w-5" />
              <span>Ethan</span>
            </a>

            <nav className="hidden md:flex items-center gap-6 text-sm">
              {navItems.map((n) => (
                <a key={n.href} href={n.href} className="hover:text-white/90 text-slate-300">
                  {n.label}
                </a>
              ))}
              <div className="ml-2 flex items-center gap-3">
                <a href="mailto:ethanw5667@gmail.com" aria-label="Email" className="p-2 rounded-xl hover:bg-slate-800">
                  <Mail className="h-5 w-5" />
                </a>
                <a href="https://github.com/" target="_blank" rel="noreferrer" aria-label="GitHub" className="p-2 rounded-xl hover:bg-slate-800">
                  <Github className="h-5 w-5" />
                </a>
                <a href="https://www.linkedin.com/" target="_blank" rel="noreferrer" aria-label="LinkedIn" className="p-2 rounded-xl hover:bg-slate-800">
                  <Linkedin className="h-5 w-5" />
                </a>
              </div>
            </nav>

            <Button variant="ghost" size="icon" className="md:hidden" onClick={() => setOpen((p) => !p)} aria-label="Toggle menu">
              {open ? <X className="h-5 w-5" /> : <Menu className="h-5 w-5" />}
            </Button>
          </div>
        </div>
        {/* Mobile menu */}
        {open && (
          <div className="md:hidden border-t border-slate-800">
            <div className="mx-auto max-w-6xl px-4 py-4 flex flex-col gap-3">
              {navItems.map((n) => (
                <a key={n.href} href={n.href} onClick={() => setOpen(false)} className="py-1 text-slate-300">
                  {n.label}
                </a>
              ))}
            </div>
          </div>
        )}
      </header>

      {/* Hero */}
      <section id="home" className="mx-auto max-w-6xl px-4 pt-16 pb-24">
        <div className="grid lg:grid-cols-2 gap-10 items-center">
          <motion.div initial={{ opacity: 0, y: 16 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }}>
            <h1 className="text-4xl md:text-5xl font-extrabold tracking-tight leading-tight">
              Hi, I’m <span className="bg-clip-text text-transparent bg-gradient-to-r from-indigo-300 via-sky-300 to-teal-200">Ethan</span>.
            </h1>
            <p className="mt-4 text-slate-300 text-lg">
              Student • Physics & Astronomy • Builder of hands-on experiments and clear explanations.
            </p>
            <div className="mt-6 flex flex-wrap gap-3">
              <Button asChild>
                <a href="#projects"><Briefcase className="mr-2 h-4 w-4"/>View Projects</a>
              </Button>
              <Button variant="secondary" asChild>
                <a href="#resume"><FileText className="mr-2 h-4 w-4"/>Resume & CV</a>
              </Button>
            </div>
          </motion.div>

          <motion.div initial={{ opacity: 0, y: 16 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.7, delay: 0.1 }} className="relative">
            <div className="aspect-square rounded-3xl bg-gradient-to-br from-indigo-500/20 via-sky-500/10 to-emerald-500/10 p-[2px]">
              <div className="w-full h-full rounded-3xl bg-slate-950/40 border border-slate-800 flex items-center justify-center">
                <div className="p-8 text-center">
                  <p className="text-sm uppercase tracking-widest text-slate-400">Featured</p>
                  <h3 className="mt-2 text-xl font-semibold">International Young Physicists’ Tournament</h3>
                  <p className="mt-2 text-slate-300">Canada Team • Experimental design, modeling, and presentation</p>
                </div>
              </div>
            </div>
          </motion.div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="mx-auto max-w-6xl px-4 py-20">
        <div className="grid md:grid-cols-2 gap-8 items-start">
          <div>
            <h2 className="text-2xl font-bold">About</h2>
            <p className="mt-4 text-slate-300 leading-relaxed">
              I’m a senior at St. Robert CHS (IB) passionate about mechanics-based physics, astronomy, and building community through hands-on learning. I’ve represented Canada at IYPT and IOAA. I like turning uncertainty into models and messy lab notes into clean insights.
            </p>
          </div>
          <Card className="bg-slate-900/50 border-slate-800">
            <CardHeader>
              <CardTitle>Highlights</CardTitle>
              <CardDescription>Recent experiences & interests</CardDescription>
            </CardHeader>
            <CardContent className="grid sm:grid-cols-2 gap-4">
              {[
                { t: "IYPT Canada — 1st (Individual)", d: "Report-based selection; Sweden team" },
                { t: "IOAA Training Camp", d: "Celestial mechanics, observation" },
                { t: "Physics Club President", d: "Workshops, contests, mentoring" },
                { t: "Basement Lab", d: "Arduino rigs, oscilloscopes, COMSOL" },
              ].map((item, i) => (
                <div key={i} className="rounded-2xl border border-slate-800 p-4 bg-slate-950/50">
                  <p className="font-medium">{item.t}</p>
                  <p className="text-sm text-slate-400">{item.d}</p>
                </div>
              ))}
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Projects */}
      <section id="projects" className="mx-auto max-w-6xl px-4 py-20">
        <h2 className="text-2xl font-bold">Projects</h2>
        <p className="mt-2 text-slate-300">A few things I’ve built or researched recently.</p>

        <div className="mt-8 grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          {[
            {
              title: "Damped Harmonic Oscillator Fitting",
              blurb: "From raw accelerometer data to parameters & R², with uncertainty propagation.",
              link: "#",
            },
            {
              title: "Arrhenius Kinetics Toolkit",
              blurb: "1/T vs ln k linearization, regression, and activation energy extraction.",
              link: "#",
            },
            {
              title: "Sky Plate Solving Notes",
              blurb: "From star field to coordinates; learning to read the sky I fly under.",
              link: "#",
            },
          ].map((p, i) => (
            <Card key={i} className="bg-slate-900/50 border-slate-800 hover:shadow-xl hover:shadow-sky-500/10 transition">
              <CardHeader>
                <CardTitle className="text-lg">{p.title}</CardTitle>
                <CardDescription>{p.blurb}</CardDescription>
              </CardHeader>
              <CardContent>
                <Button asChild variant="secondary" className="w-full">
                  <a href={p.link}>
                    <Github className="mr-2 h-4 w-4" /> View Repo / Doc
                  </a>
                </Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Resume & CV */}
      <section id="resume" className="mx-auto max-w-6xl px-4 py-20">
        <h2 className="text-2xl font-bold">Resume & CV</h2>
        <p className="mt-2 text-slate-300">Placeholders for now — upload or link later.</p>

        <div className="mt-8 grid md:grid-cols-2 gap-6">
          <Card className="bg-slate-900/50 border-slate-800">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><FileText className="h-5 w-5"/>Resume</CardTitle>
              <CardDescription>One-page snapshot</CardDescription>
            </CardHeader>
            <CardContent className="space-y-4">
              <div className="rounded-xl border border-dashed border-slate-700 p-6 text-center">
                <p className="text-slate-400">No file yet. Add a PDF link later.</p>
              </div>
              <div className="flex gap-3">
                <Button variant="secondary" disabled><Download className="mr-2 h-4 w-4"/>Download PDF</Button>
                <Button variant="outline" disabled>Open in New Tab</Button>
              </div>
            </CardContent>
          </Card>

          <Card className="bg-slate-900/50 border-slate-800">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><GraduationCap className="h-5 w-5"/>Curriculum Vitae</CardTitle>
              <CardDescription>Expanded academic CV</CardDescription>
            </CardHeader>
            <CardContent className="space-y-4">
              <div className="rounded-xl border border-dashed border-slate-700 p-6 text-center">
                <p className="text-slate-400">No file yet. Add a PDF link later.</p>
              </div>
              <div className="flex gap-3">
                <Button variant="secondary" disabled><Download className="mr-2 h-4 w-4"/>Download PDF</Button>
                <Button variant="outline" disabled>Open in New Tab</Button>
              </div>
            </CardContent>
          </Card>
        </div>

        <p className="mt-4 text-sm text-slate-400">When you’re ready, I’ll replace the placeholders with real links and add an inline viewer.</p>
      </section>

      {/* Contact */}
      <section id="contact" className="mx-auto max-w-6xl px-4 py-20">
        <div className="grid md:grid-cols-2 gap-8">
          <div>
            <h2 className="text-2xl font-bold">Contact</h2>
            <p className="mt-2 text-slate-300">Have a question or want to collaborate? Send a note.</p>
            <div className="mt-4 flex gap-3">
              <Button asChild variant="secondary"><a href="mailto:ethanw5667@gmail.com"><Mail className="mr-2 h-4 w-4"/>Email</a></Button>
              <Button asChild variant="outline"><a href="https://www.linkedin.com/" target="_blank" rel="noreferrer"><Linkedin className="mr-2 h-4 w-4"/>LinkedIn</a></Button>
            </div>
          </div>

          <Card className="bg-slate-900/50 border-slate-800">
            <CardHeader>
              <CardTitle>Quick Message</CardTitle>
              <CardDescription>Uses your default mail app</CardDescription>
            </CardHeader>
            <CardContent>
              <form action="mailto:ethanw5667@gmail.com" method="post" encType="text/plain" className="space-y-3">
                <Input placeholder="Your name" name="name" required />
                <Input placeholder="Your email" name="email" type="email" required />
                <Textarea placeholder="Message" name="message" rows={5} required />
                <Button type="submit">Send</Button>
              </form>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-slate-800">
        <div className="mx-auto max-w-6xl px-4 py-10 flex flex-col md:flex-row items-center justify-between gap-4">
          <p className="text-sm text-slate-400">© {new Date().getFullYear()} Ethan. All rights reserved.</p>
          <div className="flex items-center gap-4 text-sm text-slate-400">
            <a href="#home" className="hover:text-slate-200">Back to top</a>
            <span className="opacity-30">•</span>
            <a href="#resume" className="hover:text-slate-200">Resume & CV</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
