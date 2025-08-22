# Brittany-Wright
import React from "react";

// Single-file React mockup for the "Healing Through Chaos" homepage
// TailwindCSS classes only. No external assets required.
// Swap the ASSET_* URLs with your hosted images later if you want real images.

const ASSET_HEADSHOT = null; // e.g., "https://.../brittany-headshot.jpg"
const ASSET_WORKBOOK = null; // e.g., "https://.../workbook-cover.png"
const ASSET_SILENT_LAYER = null; // article art
const ASSET_PATTERN_RECOG = null; // article art
const ASSET_MOTHER_SOVEREIGN = null; // kit mockup

export default function PreviewSite() {
  return (
    <div className="min-h-screen w-full bg-[#0b0f14] text-slate-100 selection:bg-cyan-300/40 selection:text-black">
      <Nav />
      <main>
        <Hero />
        <Products />
        <Resources />
        <Newsletter />
        <Contact />
        <Footer />
      </main>
    </div>
  );
}

function Nav() {
  return (
    <header className="sticky top-0 z-30 backdrop-blur supports-[backdrop-filter]:bg-black/40 bg-black/30 border-b border-white/10">
      <div className="mx-auto max-w-6xl px-4 py-3 flex items-center justify-between">
        <div className="flex items-center gap-3">
          <div className="h-8 w-8 rounded-xl bg-gradient-to-br from-cyan-400 to-fuchsia-500 shadow-lg shadow-cyan-500/20" />
          <span className="font-semibold tracking-wide">Healing Through Chaos</span>
        </div>
        <nav className="hidden md:flex items-center gap-6 text-sm text-slate-300">
          <a href="#products" className="hover:text-white">Products</a>
          < href="#resources" className="hover:text-white">Resources</a>
          <a href="#newsletter" className="hover:text-white">Newsletter</a>
          <a href="#contact" className="hover:text-white">Contact</a>
          <a href="#" className="rounded-xl px-3 py-1.5 bg-white/10 hover:bg-white/20 text-white border border-white/10">Work with Me</a>
        </nav>
      </div>
    </header>
  );
}

function Hero() {
  return (
    <section className="relative overflow-hidden">
      <GridGlow />
      <div className="relative mx-auto max-w-6xl px-4 pt-20 pb-16 md:pt-28 md:pb-24">
        <div className="grid md:grid-cols-2 gap-10 items-center">
          <div>
            <div className="inline-flex items-center gap-2 rounded-full border border-cyan-400/30 bg-cyan-400/10 px-3 py-1 text-xs text-cyan-200">
              <span className="h-1.5 w-1.5 rounded-full bg-cyan-300" />
              Trauma-informed Systems • Cyber-calm design
            </div>
            <h1 className="mt-4 text-4xl md:text-5xl font-bold tracking-tight">
              Heal. Systematize. <span className="bg-gradient-to-r from-cyan-300 via-teal-200 to-fuchsia-300 bg-clip-text text-transparent">Lead.</span>
            </h1>
            <p className="mt-4 text-slate-300 md:text-lg max-w-prose">
              A premium framework for recovery that turns lived experience into a sovereign system. Tools that respect your nervous system and protect your signal.
            </p>
            <div className="mt-6 flex flex-wrap gap-3">
              <a href="#products" className="rounded-2xl bg-cyan-500/20 hover:bg-cyan-500/30 border border-cyan-300/30 px-4 py-2 font-medium text-cyan-100 shadow-md shadow-cyan-500/10">Explore Products</a>
              <a href="#contact" className="rounded-2xl bg-white/10 hover:bg-white/20 border border-white/10 px-4 py-2 font-medium">Book Collaboration</a>
            </div>
            <div className="mt-6 flex items-center gap-6 text-xs text-slate-400">
              <Badge>Evidence-led</Badge>
              <Badge>Zero-fluff</Badge>
              <Badge>Built for Mothers</Badge>
            </div>
          </div>
          <div className="relative">
            <CardImage title="Brittany Wright" subtitle="Behavioral Signal Sovereign">
              {ASSET_HEADSHOT ? (
                <img src={ASSET_HEADSHOT} alt="Brittany headshot" className="h-full w-full object-cover" />
              ) : (
                <EmptyImageLabel>Headshot Placeholder</EmptyImageLabel>
              )}
            </CardImage>
          </div>
        </div>
      </div>
    </section>
  );
}

function Products() {
  return (
    <section id="products" className="relative py-16 md:py-20 border-t border-white/10">
      <div className="mx-auto max-w-6xl px-4">
        <SectionTitle kicker="Offers">Products</SectionTitle>
        <div className="grid md:grid-cols-3 gap-6 mt-8">
          <ProductCard title="Healing Through Chaos — 30-Day System" blurb="A step-by-step trauma recovery workbook with four phases: Safety, Awareness, Integration, and Empowerment." cta="View Workbook">
            {ASSET_WORKBOOK ? (
              <img src={ASSET_WORKBOOK} alt="Workbook cover" className="h-full w-full object-cover" />
            ) : (
              <EmptyImageLabel>Workbook Cover</EmptyImageLabel>
            )}
          </ProductCard>
          <ProductCard title="Mother Sovereign Protection Kit" blurb="Full-spectrum safeguarding: emotional, digital, legal, and spiritual protocols from birth to adulthood." cta="See the Kit">
            {ASSET_MOTHER_SOVEREIGN ? (
              <img src={ASSET_MOTHER_SOVEREIGN} alt="Mother Sovereign Kit" className="h-full w-full object-cover" />
            ) : (
              <EmptyImageLabel>Kit Mockup</EmptyImageLabel>
            )}
          </ProductCard>
          <ProductCard title="Silent Layer Sessions" blurb="1:1 strategy for signal hygiene, narrative control, and platform positioning without burnout." cta="Book a Session">
            <div className="flex h-full w-full items-center justify-center">
              <div className="text-slate-400 text-sm">Session Visual</div>
            </div>
          </ProductCard>
        </div>
      </div>
    </section>
  );
}

function Resources() {
  return (
    <section id="resources" className="relative py-16 md:py-20 border-t border-white/10">
      <div className="mx-auto max-w-6xl px-4">
        <SectionTitle kicker="Writing">Resources & Essays</SectionTitle>
        <div className="grid md:grid-cols-2 gap-6 mt-8">
          <ArticleCard title="The Silent Layer" tag="Essay">
            {ASSET_SILENT_LAYER ? (
              <img src={ASSET_SILENT_LAYER} alt="Silent Layer" className="h-full w-full object-cover" />
            ) : (
              <EmptyImageLabel>Article Art</EmptyImageLabel>
            )}
          </ArticleCard>
          <ArticleCard title="Pattern Recognition" tag="Field Notes">
            {ASSET_PATTERN_RECOG ? (
              <img src={ASSET_PATTERN_RECOG} alt="Pattern Recognition" className="h-full w-full object-cover" />
            ) : (
              <EmptyImageLabel>Article Art</EmptyImageLabel>
            )}
          </ArticleCard>
        </div>
      </div>
    </section>
  );
}

function Newsletter() {
  return (
    <section id="newsletter" className="relative py-16 md:py-20 border-t border-white/10">
      <div className="mx-auto max-w-6xl px-4">
        <SectionTitle kicker="Stay in the loop">Newsletter</SectionTitle>
        <div className="mt-6 grid md:grid-cols-3 gap-6">
          <div className="md:col-span-2 text-slate-300">
            Get one strong signal per week: zero spam, zero fluff. Essays, tools, and release notes.
          </div>
          <form className="flex gap-3">
            <input type="email" placeholder="you@domain.com" className="w-full rounded-xl bg-white/5 border border-white/10 px-4 py-3 text-white placeholder:text-slate-400 focus:outline-none focus:ring-2 focus:ring-cyan-400" />
            <button type="button" className="rounded-xl px-4 py-3 bg-cyan-500/20 border border-cyan-300/30 hover:bg-cyan-500/30 font-medium">Subscribe</button>
          </form>
        </div>
      </div>
    </section>
  );
}

function Contact() {
  return (
    <section id="contact" className="relative py-16 md:py-20 border-t border-white/10">
      <div className="mx-auto max-w-6xl px-4">
        <SectionTitle kicker="Collaborations">Contact</SectionTitle>
        <div className="grid md:grid-cols-2 gap-6 mt-6">
          <div className="space-y-3 text-slate-300">
            <p>Speaking, licensing, or strategic partnerships? Drop your details and a short brief. We reply to aligned requests only.</p>
            <ul className="text-sm list-disc pl-5 text-slate-400 space-y-1">
              <li>Topics: trauma-informed tech, authorship rights, emotional infrastructure</li>
              <li>Formats: keynotes, workshops, advisory, media</li>
            </ul>
          </div>
          <form className="space-y-3">
            <input placeholder="Name" className="w-full rounded-xl bg-white/5 border border-white/10 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-cyan-400" />
            <input placeholder="Email" className="w-full rounded-xl bg-white/5 border border-white/10 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-cyan-400" />
            <textarea placeholder="Tell me about your project" rows={5} className="w-full rounded-xl bg-white/5 border border-white/10 px-4 py-3 focus:outline-none focus:ring-2 focus:ring-cyan-400" />
            <button type="button" className="rounded-xl px-4 py-3 bg-white/10 border border-white/10 hover:bg-white/20 font-medium">Send</button>
          </form>
        </div>
      </div>
    </section>
  );
}

function Footer() {
  return (
    <footer className="border-t border-white/10">
      <div className="mx-auto max-w-6xl px-4 py-10 text-sm text-slate-400 flex flex-col md:flex-row items-center justify-between gap-4">
        <div className="opacity-80">© {new Date().getFullYear()} Brittany Wright — Behavioral Signal Sovereign</div>
        <div className="flex items-center gap-4">
          <a href="#" className="hover:text-white">Terms</a>
          <a href="#" className="hover:text-white">Privacy</a>
          <a href="#" className="hover:text-white">Licensing</a>
        </div>
      </div>
    </footer>
  );
}

function SectionTitle({ kicker, children }) {
  return (
    <div>
      <div className="text-xs tracking-widest text-cyan-300/80 uppercase">{kicker}</div>
      <h2 className="mt-2 text-2xl md:text-3xl font-semibold">{children}</h2>
    </div>
  );
}

function ProductCard({ title, blurb, cta, children }) {
  return (
    <div className="group rounded-2xl overflow-hidden border border-white/10 bg-gradient-to-b from-white/5 to-white/[0.03] hover:from-white/10 hover:to-white/[0.05] transition shadow-lg shadow-black/20">
      <div className="aspect-[4/3] bg-white/5 flex items-center justify-center">
        <div className="h-full w-full">{children}</div>
      </div>
      <div className="p-4">
        <div className="font-medium text-lg">{title}</div>
        <p className="mt-1 text-sm text-slate-400 min-h-[44px]">{blurb}</p>
        <div className="mt-3">
          <a className="inline-flex items-center gap-2 rounded-xl border border-cyan-300/30 bg-cyan-500/10 px-3 py-1.5 hover:bg-cyan-500/20">
            <span className="text-sm">{cta}</span>
            <svg className="h-4 w-4" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M5 12h14M13 5l7 7-7 7" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"/></svg>
          </a>
        </div>
      </div>
    </div>
  );
}

function ArticleCard({ title, tag, children }) {
  return (
    <div className="group rounded-2xl overflow-hidden border border-white/10 bg-gradient-to-b from-white/5 to-white/[0.03] hover:from-white/10 hover:to-white/[0.05] transition">
      <div className="aspect-[21/9] bg-white/5 flex items-center justify-center">
        <div className="h-full w-full">{children}</div>
      </div>
      <div className="p-4">
        <div className="text-xs text-cyan-300/80">{tag}</div>
        <div className="font-medium text-lg">{title}</div>
        <p className="mt-1 text-sm text-slate-400">Read the latest from the field — essays that blend systems, story, and sovereignty.</p>
      </div>
    </div>
  );
}

function Badge({ children }) {
  return (
    <span className="inline-flex items-center gap-2 rounded-full bg-white/5 border border-white/10 px-3 py-1 mr-1">
      <span className="h-1.5 w-1.5 rounded-full bg-cyan-300" />
      <span className="text-xs text-slate-300">{children}</span>
    </span>
  );
}

function CardImage({ title, subtitle, children }) {
  return (
    <div className="relative rounded-3xl overflow-hidden border border-white/10 bg-gradient-to-br from-white/5 to-white/[0.02] shadow-2xl shadow-cyan-500/10">
      <div className="aspect-[4/5]">
        {children}
      </div>
      <div className="absolute inset-0 pointer-events-none">
        <div className="absolute inset-0 opacity-20 bg-[radial-gradient(circle_at_30%_20%,#67e8f9_0%,transparent_35%),radial-gradient(circle_at_70%_80%,#f0abfc_0%,transparent_40%)]" />
      </div>
      <div className="absolute bottom-0 left-0 right-0 p-4 bg-gradient-to-t from-black/60 to-transparent">
        <div className="text-sm text-slate-200 font-medium">{title}</div>
        <div className="text-xs text-slate-400">{subtitle}</div>
      </div>
    </div>
  );
}

function EmptyImageLabel({ children }) {
  return (
    <div className="flex h-full w-full items-center justify-center">
      <div className="text-slate-400 text-sm">{children}</div>
    </div>
  );
}

function GridGlow() {
  return (
    <div aria-hidden className="pointer-events-none absolute inset-0">
      {/* Cyan/Fuchsia corner glows */}
      <div className="absolute -top-32 -right-40 h-96 w-96 rounded-full blur-3xl bg-cyan-500/20" />
      <div className="absolute -bottom-24 -left-40 h-96 w-96 rounded-full blur-3xl bg-fuchsia-500/20" />
      {/* Subtle grid */}
      <div className="absolute inset-0 opacity-[0.08]" style={{
        backgroundImage:
          "linear-gradient(to right, rgba(255,255,255,.2) 1px, transparent 1px), linear-gradient(to bottom, rgba(255,255,255,.2) 1px, transparent 1px)",
        backgroundSize: "48px 48px",
      }} />
    </div>
  );
}

